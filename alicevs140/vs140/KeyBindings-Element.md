---
title: "KeyBindings Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 26a15d5c-ddea-4977-af7f-d795ff09c7ad
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# KeyBindings Element
The KeyBindings element groups KeyBinding elements and other KeyBindings groupings.  
  
## Syntax  
  
```  
<KeyBindings>  
  <KeyBinding>... </KeyBinding>  
  <KeyBinding>... </KeyBinding>  
</KeyBindings>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|Condition|Optional. See [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[KeyBinding](../vs140/KeyBinding-Element.md)|Specifies keyboard shortcuts for the commands.|  
|[KeyBindings](../vs140/KeyBindings-Element.md)|Groups KeyBinding elements and other KeyBindings groupings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[CommandTable](../vs140/CommandTable-Element.md)|Defines all the elements that represent commands.|  
  
## Example  
  
```  
<KeyBindings>  
  <KeyBinding guid="guidWidgetPackage" id="cmdidUpdateWidget"   
    editor="guidWidgetEditor" key1="VK_F5"/>  
  <KeyBinding guid="guidWidgetPackage" id="cmdidRunWidget"   
    editor="guidWidgetEditor" key1="VK_F5" mod1="Control"/>  
</KeyBindings>  
```  
  
## See Also  
 [KeyBinding](../vs140/KeyBinding-Element.md)   
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)