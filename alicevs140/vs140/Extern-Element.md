---
title: "Extern Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db6c3ddd-a1ba-450a-897a-bb568a5377fc
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Extern Element
The Extern element references any external header (.h) files to merge with the .vsct file at compile time. The files to be merged must be on the Include path given to the VSCT compiler or referenced by an [Include element](../vs140/Include-Element.md). The files may be other .vsct files or C++ header files.  
  
 Definitions in header files must be of the form "#define [Symbol] [Value]"  The value may be another symbol if it is previously defined. Definitions may be used in conditional statements of command items. Any symbol not actually used will be discarded.  
  
 CommandTable Element  
Extern Element  
  
## Syntax  
  
```  
<Extern href="stdidcmd.h" />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|href|Required. The path to the header file:<br /><br /> href="stdidcmd.h"|  
|Condition|Optional. See [Conditional Attributes](../vs140/VSCT-XML-Schema-Conditional-Attributes.md).|  
|language|Optional. The default language of all [<Strings\>](../vs140/Strings-Element.md) elements in the command table:<br /><br /> language="en-us"|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|None.|None.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[CommandTable Element](../vs140/CommandTable-Element.md)|Defines all of the elements that represent commands — that is, menu items, menus, toolbars, and combo boxes — that a VSPackage provides to the IDE.|  
  
## Example  
  
```  
<?xml version="1.0" encoding="utf-8"?>  
<CommandTable xmlns="http://schemas.microsoft.com/VisualStudio/2005-10-  
  18/CommandTable" xmlns:xs="http://www.w3.org/2001/XMLSchema">  
    <Extern href="C:\VSCore\vscommon\inc\vsshlids.h"/>  
    …  
  <Commands package="guidMyPackage">  
</CommandTable>  
```  
  
## See Also  
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)   
 [How VSPackages Contribute User Interface Elements](../Topic/How%20VSPackages%20Add%20User%20Interface%20Elements.md)   
 [Menu and Toolbar Commands](../Topic/Commands,%20Menus,%20and%20Toolbars.md)