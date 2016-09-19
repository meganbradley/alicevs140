---
title: "Button Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96dccf51-2b00-4700-9d28-924b34c21ecd
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Button Element
Defines an element that the user can interact with. Buttons can be of different kinds: Button, MenuButton, and SplitDropDown.  
  
## Syntax  
  
```  
<Button guid="guidMyCommandSet" id="MyCommand" priority="0x102" type="button">  
  <Parent>... </Parent>  
  <Icon>... </Icon>  
  <CommandFlag>... </CommandFlag>  
  <Strings>... </Strings>  
</Button>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|guid|Required. GUID of the GUID/ID command identifier.|  
|id|Required. ID of the GUID/ID command identifier.|  
|priority|Optional. A numeric value that specifies the priority.|  
|type|Optional. An enumerated value that specifies the kind of button.<br /><br /> If not given, uses Button.<br /><br /> Button<br /> A standard command that appears on toolbars (typically as an iconic button), menus, and context menus.<br /><br /> MenuButton<br /> A menu item that does not execute a command, but produces another menu.<br /><br /> SplitDropDown<br /> Controls, such as the Undo and Redo buttons on the standard toolbar in Microsoft Word.|  
|Condition|Optional. See [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Parent](../vs140/Parent-Element.md)|Optional. The parent element of the button.|  
|[Icon](../vs140/Icon-Element.md)|Optional. The icon associated with the button.|  
|[CommandFlag](../vs140/Command-Flag-Element.md)|Required. The valid CommandFlag values for a Button are as follows.<br /><br /> - AllowParams<br /><br /> - CommandWellOnly<br /><br /> - DefaultDisabled<br /><br /> - DefaultInvisible<br /><br /> - DontCache<br /><br /> - DynamicItemStart<br /><br /> - DynamicVisibility<br /><br /> - FixMenuController<br /><br /> - IconAndText<br /><br /> - NoButtonCustomize<br /><br /> - NoCustomize<br /><br /> - NoKeyCustomize<br /><br /> - NoShowOnMenuController<br /><br /> - Pict<br /><br /> - PostExec<br /><br /> - ProfferedCmd<br /><br /> - RouteToDocs<br /><br /> - TextCascadeUseBtn<br /><br /> - TextMenuUseButton<br /><br /> - TextChanges<br /><br /> - TextChangesButton<br /><br /> - TextContextUseButton<br /><br /> - TextMenuCtrlUseMenu<br /><br /> - TextMenuUseButton<br /><br /> - TextOnly|  
|[Strings](../vs140/Strings-Element.md)|Required. The child [ButtonText element](../vs140/ButtonText-Element.md) must be defined.|  
|Annotation|Optional comment.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Buttons](../vs140/Buttons-Element.md)|Groups Button elements.|  
  
## Example  
 The following example defines a button in a .vsct file.  
  
 [!CODE [MenuText#02](../CodeSnippet/VS_Snippets_VSSDK/menutext#02)]  
  
## See Also  
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)