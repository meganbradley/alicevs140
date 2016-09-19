---
title: "PreviewImage Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d1796f20-523b-4e0d-8ac3-ca87f3b5a9b6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PreviewImage Element (Visual Studio Templates)
Specifies the preview image, as a file name, for the preview image that will appear in either the **New Project** or **Add New Item** dialog box.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <PreviewImage\>  
  
## Syntax  
  
```  
<PreviewImage>"filename"</PreviewImage>  
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
  
 The text must be a string that represents a file name.  
  
## Remarks  
 `PreviewImage` is an optional element.  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)