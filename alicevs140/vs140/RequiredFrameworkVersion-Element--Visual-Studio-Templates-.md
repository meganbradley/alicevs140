---
title: "RequiredFrameworkVersion Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 08a4f609-51a5-4723-b89f-99277fb18871
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RequiredFrameworkVersion Element (Visual Studio Templates)
Specifies the minimum .NET Framework version that is required by the template.Schema Hierarchy.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <RequiredFrameworkVersion\>  
  
## Syntax  
  
```  
<RequiredFrameworkVersion> .... </RequiredFrameworkVersion>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Categorizes the template and defines how it is displayed in either the **New Project** or the **Add New Item** dialog box.|  
  
## Text Value  
 A text value is required.  
  
 The text must be the minimum version number of the .NET Framework that is required for the template.  
  
## Remarks  
 `RequiredFrameworkVersion` is an optional element. Use this element if the template only supports a specific minimum version, and later versions if any, of the .NET Framework.  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [Targeting a Specific .NET Framework Version or Profile](../vs140/Targeting-a-Specific-.NET-Framework-Version.md)