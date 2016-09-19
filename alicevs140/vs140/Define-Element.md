---
title: "Define Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5aee74e3-de41-4dc6-9618-93e158af56dd
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Define Element
Defines a symbol name and value pair. This symbol can be evaluated by conditional attributes. For more information, see [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md). See also the [Symbols element](../vs140/Symbols-Element.md).  
  
## Syntax  
  
```  
<Define name="Mode" value="Standard" />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|name|Required. The name of the symbol:<br /><br /> name="Mode"|  
|value|Required. The value of the symbol:<br /><br /> value="Standard"|  
|Condition|Optional. For more information, see [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[CommandTable Element](../vs140/CommandTable-Element.md)|Defines all the elements that represent commands that a VSPackage provides to the integrated development environment (IDE). For example, menu items, menus, toolbars, and combo boxes.|  
  
## Example  
  
```  
<Define name="DEMO_UI"/>  
<Define name="MODE" value="Standard"/>  
```  
  
## See Also  
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)