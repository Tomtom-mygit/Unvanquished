# Create libRocket.

set(Core_HDR_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorFirstOfType.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledBoxInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementStyle.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementStyleCache.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ContextInstancerDefault.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserKeyword.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementDefinition.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorOnlyChild.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorNoneInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledHorizontal.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledImageInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PluginRegistry.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorEmpty.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetParser.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerTemplate.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyShorthandDefinition.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthOfType.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementTextDefault.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelector.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectShadowInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorLastOfType.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayoutRow.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementBackground.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserString.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureResource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNode.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Clock.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledImage.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledVerticalInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorLastChild.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementHandle.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventDispatcher.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Pool.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TemplateCache.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Template.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventIterators.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerBody.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutBlockBox.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/WidgetSlider.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutInlineBoxText.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFaceLayer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementImage.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFamily.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiled.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserColour.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLParseTools.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/WidgetSliderScroll.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutBlockBoxSpace.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DocumentHeader.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/precompiled.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthLastChild.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorFirstChild.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutLineBox.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DebugFont.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectNone.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectShadow.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureDatabase.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserNumber.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledVertical.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthChild.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayoutRectangle.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutInlineBox.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/GeometryDatabase.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectOutlineInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayoutTexture.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFace.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayout.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventInstancerDefault.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementBorder.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerHead.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementDecoration.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StreamFile.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutEngine.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectOutline.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetFactory.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthLastOfType.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FileInterfaceDefault.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerDefault.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorNone.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledHorizontalInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StringCache.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectNoneInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledBox.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorOnlyOfType.h
)

set(Core_PUB_HDR_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/FontEffect.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/TypeConverter.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementScroll.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/SystemInterface.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Colour.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Box.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ConvolutionFilter.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/EventListenerInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementInstancerGeneric.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/FileInterface.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/MathTypes.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/PropertySpecification.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Property.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Plugin.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementReference.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/StreamMemory.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/WString.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/EventListener.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/PropertyDefinition.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Decorator.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Texture.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/PropertyDictionary.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/StyleSheet.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/FontGlyph.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ReferenceCountable.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/StringUtilities.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Vertex.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementUtilities.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Factory.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Stream.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/GeometryUtilities.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Vector2.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/StyleSheetSpecification.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/RenderInterface.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/StyleSheetKeywords.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Core.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/FontDatabase.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Header.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Dictionary.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Types.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/XMLParser.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementDocument.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/BaseXMLParser.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Debug.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/URL.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Input.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Event.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Geometry.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Font.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ElementText.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/String.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Element.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ScriptInterface.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/StringBase.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/EventInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/DecoratorInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Context.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/FontEffectInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Variant.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Math.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Log.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/Platform.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/XMLNodeHandler.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/PropertyParser.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/ContextInstancer.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/UnicodeRange.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core/FontFaceHandle.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Core.h
)

set(Core_SRC_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StreamMemory.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledVertical.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventInstancerDefault.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementHandle.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerBody.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureDatabase.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledBox.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetParser.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Core.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Template.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandler.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/String.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ReferenceCountable.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorLastOfType.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementBackground.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledHorizontal.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventDispatcher.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventListenerInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StringCache.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementUtilities.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TemplateCache.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledBoxInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Event.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Clock.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/GeometryDatabase.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorOnlyChild.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementDecoration.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffect.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FileInterfaceDefault.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerTemplate.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ConvolutionFilter.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiled.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerHead.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DocumentHeader.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ContextInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Decorator.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/BaseXMLParser.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Box.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyDefinition.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Math.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementText.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/precompiled.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetSpecification.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectNone.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PluginRegistry.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/RenderInterface.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ContextInstancerDefault.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutInlineBoxText.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayout.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyDictionary.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Context.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutEngine.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/WidgetSlider.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Property.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementStyle.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementStyleCache.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorNoneInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Element.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectOutlineInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontDatabase.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Texture.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementScroll.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFaceLayer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/UnicodeRange.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FileInterface.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthLastChild.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectShadow.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetFactory.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorLastChild.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutBlockBoxSpace.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectNoneInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFace.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Vector2.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserKeyword.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNode.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementDocument.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorEmpty.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledImageInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectOutline.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFamily.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/WString.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/URL.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontEffectShadowInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledHorizontalInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorNone.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StreamFile.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Dictionary.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledImage.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/EventInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayoutRow.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertySpecification.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/FontFaceHandle.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/SystemInterface.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementBorder.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Plugin.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutLineBox.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayoutRectangle.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureResource.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutBlockBox.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthOfType.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementImage.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelector.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/GeometryUtilities.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthLastOfType.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/WidgetSliderScroll.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLParseTools.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorFirstOfType.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementTextDefault.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserNumber.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLNodeHandlerDefault.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/TextureLayoutTexture.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Stream.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/XMLParser.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheet.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorFirstChild.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StringUtilities.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Log.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Variant.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorNthChild.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Geometry.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/DecoratorTiledVerticalInstancer.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementReference.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/StyleSheetNodeSelectorOnlyOfType.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserString.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/PropertyParserColour.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/Factory.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/ElementDefinition.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Core/LayoutInlineBox.cpp
)

set(Controls_HDR_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetDropDown.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeRange.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetSliderInput.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInputSingleLine.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInput.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeButton.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetSlider.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInputMultiLine.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/XMLNodeHandlerTabSet.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeCheckbox.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeSubmit.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeRadio.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementTextSelection.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputType.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/XMLNodeHandlerDataGrid.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/XMLNodeHandlerTextArea.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInputSingleLinePassword.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeText.h
)

set(Controls_PUB_HDR_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/DataQuery.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementFormControlDataSelect.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementFormControlTextArea.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementTabSet.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/Controls.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementFormControlSelect.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/SelectOption.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementFormControlInput.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementFormControl.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/Header.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/DataSource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementDataGrid.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementDataGridExpandButton.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementDataGridRow.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/Clipboard.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/DataFormatter.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/DataSourceListener.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementForm.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls/ElementDataGridCell.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Controls.h
)

set(Controls_SRC_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/SelectOption.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInputSingleLinePassword.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/XMLNodeHandlerDataGrid.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/XMLNodeHandlerTextArea.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetDropDown.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementTabSet.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementFormControlTextArea.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/Clipboard.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInputMultiLine.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/DataSourceListener.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetSliderInput.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementFormControlDataSelect.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeSubmit.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInput.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/Controls.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeRadio.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementDataGridRow.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementFormControlSelect.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetSlider.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementDataGridExpandButton.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeText.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeCheckbox.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputType.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementFormControlInput.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementDataGrid.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementTextSelection.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/XMLNodeHandlerTabSet.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/DataQuery.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementForm.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeButton.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/InputTypeRange.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementDataGridCell.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/ElementFormControl.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/WidgetTextInputSingleLine.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/DataFormatter.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Controls/DataSource.cpp
)

set(Debugger_HDR_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/ElementLog.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/SystemInterface.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/InfoSource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/Plugin.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/LogSource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/ElementInfo.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/BeaconSource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/Geometry.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/MenuSource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/ElementContextHook.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/CommonSource.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/FontSource.h
)

set(Debugger_PUB_HDR_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Debugger/Header.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Debugger/Debugger.h
    ${CMAKE_CURRENT_SOURCE_DIR}/Include/Rocket/Debugger.h
)

set(Debugger_SRC_FILES
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/ElementInfo.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/Debugger.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/ElementLog.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/ElementContextHook.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/SystemInterface.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/Plugin.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/Source/Debugger/Geometry.cpp
)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE "Release/${GAMELIB_OUTPUT_DIR}")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG "Debug/${GAMELIB_OUTPUT_DIR}")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_MINSIZEREL "MinSizeRel/${GAMELIB_OUTPUT_DIR}")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELWITHDEBINFO "RelWithDebInfo/${GAMELIB_OUTPUT_DIR}")

if (NOT FREETYPE_INCLUDE_DIRS)
    find_package(Freetype REQUIRED)
endif()
include_directories(${FREETYPE_INCLUDE_DIRS})

set(ROCKET_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR}/Include)
set(ROCKET_INCLUDE_DIRS ${ROCKET_INCLUDE_DIRS} PARENT_SCOPE)
include_directories(${ROCKET_INCLUDE_DIRS})
add_library(ROCKET_LIB STATIC
    ${Core_HDR_FILES}       ${Core_PUB_HDR_FILES}       ${Core_SRC_FILES}
    ${Controls_HDR_FILES}   ${Controls_PUB_HDR_FILES}   ${Controls_SRC_FILES}
    ${Debugger_HDR_FILES}   ${Debugger_PUB_HDR_FILES}   ${Debugger_SRC_FILES}
)

set_property(TARGET ROCKET_LIB PROPERTY
    COMPILE_DEFINITIONS ROCKET_STATIC_LIB
)
set_target_properties(ROCKET_LIB PROPERTIES
    POSITION_INDEPENDENT_CODE 1
)
