---
title: "Groups Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 740ca4ec-79fa-4b98-8f9a-2a137f9f7f98
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Groups Element
Contains entries that define the command groups of a VSPackage.  
  
## Syntax  
  
```  
<Groups>  
  <Group>... </Group>  
  <Group>... </Group>  
</Groups>  
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
|[Group Element](../vs140/Group-Element.md)|Represents a single command group.|  
|[Groups Element](../vs140/Groups-Element.md)|Contains entries that define the command groups of a VSPackage.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Commands](../vs140/Commands-Element.md)|Represents the collection of commands on the VSPackage toolbar.|  
  
## Example  
  
```  
<Groups>  
  <Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">  
    <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>  
  </Group>  
</Groups>  
```  
  
## See Also  
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)   
 [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md)