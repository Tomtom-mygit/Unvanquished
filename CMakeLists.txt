# Unvanquished BSD Source Code
# Copyright (c) 2013-2014, Unvanquished Developers
# All rights reserved.
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions are met:
#  * Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
#  * Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in the
#    documentation and/or other materials provided with the distribution.
#  * Neither the name of the <organization> nor the
#    names of its contributors may be used to endorse or promote products
#    derived from this software without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
# ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
# WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
# DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY
# DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
# (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
# LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
# ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
# (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
# SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

cmake_minimum_required(VERSION 2.8)
project(Unvanquished C CXX)

set(Daemon_OUT ${CMAKE_CURRENT_BINARY_DIR})
add_subdirectory(daemon daemon_build)
include(DaemonGame)

set(LIB_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs)
include_directories(${LIB_DIR})

set(GAMELOGIC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
include_directories(${GAMELOGIC_DIR})
include(src.cmake)

set(NACL_DEPS_VERSION 2)
set(NACL_DEPS_DIR ${CMAKE_CURRENT_SOURCE_DIR}/external_deps/pnacl-${NACL_DEPS_VERSION})
# Download them if they not available
if (NOT EXISTS ${NACL_DEPS_DIR})
    file(MAKE_DIRECTORY ${NACL_DEPS_DIR})
    set(OBJ_DIR ${CMAKE_BINARY_DIR}${CMAKE_FILES_DIRECTORY})
    get_filename_component(BASENAME ${NACL_DEPS_DIR} NAME)
    set(REMOTE "http://dl.unvanquished.net/deps/${BASENAME}.zip")
    message(STATUS "Downloading dependencies from '${REMOTE}'")
    file(DOWNLOAD ${REMOTE} ${OBJ_DIR}/${BASENAME}.zip
        SHOW_PROGRESS
        STATUS DOWNLOAD_RESULT
        LOG DOWNLOAD_LOG
    )
    list(GET DOWNLOAD_RESULT 0 DOWNLOAD_STATUS)
    list(GET DOWNLOAD_RESULT 1 DOWNLOAD_STRING)
    if (NOT DOWNLOAD_STATUS EQUAL 0)
        message(FATAL_ERROR "Error downloading '${REMOTE}':
            Status code: ${DOWNLOAD_STATUS}
            Error string: ${DOWNLOAD_STRING}
            Download log: ${DOWNLOAD_LOG}"
        )
    endif()
    message(STATUS "Download completed successfully")

    # Extract the downloaded archive
    execute_process(
        COMMAND ${CMAKE_COMMAND} -E tar xzf ${OBJ_DIR}/${BASENAME}.zip
        WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/external_deps
        RESULT_VARIABLE EXTRACT_RESULT
    )
    if (NOT EXTRACT_RESULT EQUAL 0)
        message(FATAL_ERROR "Could not extract ${BASENAME}.zip")
    endif()
endif()

if (NACL)
    set(FREETYPE_LIBRARY ${NACL_DEPS_DIR}/libfreetype.a)
    set(FREETYPE_LIBRARIES ${FREETYPE_LIBRARY} ${NACL_DEPS_DIR}/libpng16.a)
    set(FREETYPE_INCLUDE_DIRS ${NACL_DEPS_DIR}/include/freetype2)
else()
    find_package(Freetype REQUIRED)
endif()
include_directories(${FREETYPE_INCLUDE_DIRS})

add_subdirectory(${LIB_DIR}/libRocket)
set_target_properties(ROCKET_LIB PROPERTIES FOLDER "libs")
include_directories(${ROCKET_INCLUDE_DIRS})

try_flag(WARNINGS           "-Wall")
try_flag(WARNINGS           "-Wextra")
if (USE_PEDANTIC)
    try_flag(WARNINGS       "-pedantic")
endif()
if (USE_WERROR)
    try_flag(WARNINGS       "-Werror")
    if (USE_PEDANTIC)
        try_flag(WARNINGS   "-pedantic-errors")
    endif()
endif()
# keep
try_flag(WARNINGS           "/wd4068")
try_flag(WARNINGS           "-Wno-pragmas")
try_flag(WARNINGS           "-Wno-unknown-pragmas")
try_flag(WARNINGS           "-W${WARNMODE}old-style-cast")
try_flag(WARNINGS           "-Woverloaded-virtual")
try_flag(WARNINGS           "-Wstrict-null-sentinel")
try_flag(WARNINGS           "-Wno-error=sign-promo")
# remove
try_flag(WARNINGS           "-Wno-error=maybe-uninitialized")
try_flag(WARNINGS           "-W${WARNMODE}missing-field-initializers")
try_flag(WARNINGS           "-W${WARNMODE}sign-compare")
try_flag(WARNINGS           "-Wno-error=switch")
try_flag(WARNINGS           "-Wno-error=unused-but-set-variable")
try_flag(WARNINGS           "-Wno-error=unused-function")
try_flag(WARNINGS           "-Wno-error=unused-parameter")
try_flag(WARNINGS           "-Wno-error=unused-private-field")

GAMEMODULE(NAME sgame
    DEFINITIONS
        BUILD_SGAME
    FLAGS
        ${WARNINGS}
    FILES
        ${SGAMELIST}
)

GAMEMODULE(NAME cgame
    DEFINITIONS
        BUILD_CGAME
    FLAGS
        ${WARNINGS}
    FILES
        ${CGAMELIST}
    LIBS
        ROCKET_LIB
        ${FREETYPE_LIBRARIES}
)
