---
title: "Symbols Element"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1cda43d8-42a5-4b1b-a3c8-cf0401c3202f
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Symbols Element
Defines GUIDs and IDs that are used by other VSCT elements. For unmanaged code, this information typically comes from the header files that are specified by [Extern elements](../vs140/Extern-Element.md). Managed code uses the child elements of the Symbols element to define this information.  
  
 If you create a .vsct file from an existing .cto file, the symbols will be generated as children of the Symbols element. For more information, see [How to: Create a .Vsct File from an Existing .Cto File](../vs140/How-to--Create-a-.Vsct-File-from-an-Existing-.Cto-File.md).  
  
 The Symbols element should not be confused with the [Define element](../vs140/Define-Element.md), which defines name-value pairs for use by the preprocessor.  
  
## Syntax  
  
```  
<Symbols>  
  <GuidSymbol>... </GuidSymbol>  
  <GuidSymbol>... </GuidSymbol>  
</Symbols>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|None||  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|GuidSymbol|Defines a GUID symbol. GuidSymbol has two required attributes: name and value. The name is the name of the symbol, and the value is the value of the GUID as a string.<br /><br /> For example:<GuidSymbol name="guidVsPackage1Pkg"   value="{c5f54698-101a-4846-84d3-dc748f9cd848}" /\>|  
|IDSymbol|Defines a symbol. IDSymbol has two required attributes: name and value. The name is the name of the symbol, and the value is the value of the symbol as a string.<br /><br /> For example:<IDSymbol name="MyMenuGroup" value="0x1020" /\>|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[CommandTable](../vs140/CommandTable-Element.md)|The root element of the .vsct file.|  
  
## Example  
  
```  
<Symbols>  
  <GuidSymbol name="guidVsPackage1Pkg" value="{c5f54698-101a-4846-84d3-dc748f9cd848}" />  
  <GuidSymbol name="guidVsPackage1CmdSet" value="{cb9dfd7f-2fcc-4a3e-aae8-f7fe30b1cfac}">  
    <IDSymbol name="MyMenuGroup" value="0x1020" />  
    <IDSymbol name="cmdidMyCommand" value="0x0100" />  
    <IDSymbol name="cmdidMyTool" value="0x0101" />  
  </GuidSymbol>  
</Symbols>  
```  
  
## See Also  
 [XML-Based Command Table Configuration (.vsct) Files](../vs140/Visual-Studio-Command-Table--.Vsct--Files.md)