---
title: "TemplateID Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6ca24b4e-0325-4a9e-855e-0cbbe7361d8f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TemplateID Element (Visual Studio Templates)
Specifies an identifier for an item template that is categorized into a group of item templates by the [TemplateGroupID](../vs140/TemplateGroupID-Element--Visual-Studio-Templates-.md) element.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <TemplateID\>  
  
## Syntax  
  
```  
<TemplateID> ... </TemplateID>  
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
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Categorizes the template and defines how it displays in either the **New Project** or the **Add New Item** dialog box.|  
  
## Text Value  
 A `string` that represents an identifier for an item template that is categorized into a group of item templates by the `TemplateGroupID` element.  
  
## Remarks  
 `TemplateID` is an optional element.  
  
 If a .vstemplate file omits the `TemplateID` element, then the [Name](../vs140/Name-Element--Visual-Studio-Templates-.md) element is used as the identifier for the template.  
  
 The value of the `TemplateID` element is used along with project system registration (HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\11.0\Projects\\) to filter templates that appear in the **Add New Item** dialog box.  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)