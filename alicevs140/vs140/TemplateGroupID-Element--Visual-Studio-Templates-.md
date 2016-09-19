---
title: "TemplateGroupID Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bce7b49a-90bc-4691-aff3-a87e209f6d83
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TemplateGroupID Element (Visual Studio Templates)
Specifies what kind of project an item templates will show up in. This element is significant when [ShowByDefault (Visual Studio Templates)](../vs140/ShowByDefault--Visual-Studio-Templates-.md) is set to `false`. When [ShowByDefault (Visual Studio Templates)](../vs140/ShowByDefault--Visual-Studio-Templates-.md) is set to `true`, then an item template is available in all project types.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <TemplateGroupID\>  
  
## Syntax  
  
```  
<TemplateGroupID> ... </TemplateGroupID>  
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
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Categorizes the template and defines how it displays in either the **New Project** or the **Add New Item** dialog box.|  
  
## Text Value  
 A text value is required.  
  
 The text specifies an identifier for a category of item templates.  
  
## Remarks  
 `TemplateGroupID` is an element.  
  
 The value of the `TemplateGroupID` element is used along with project system registration (HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\\*<version number\>*\Projects\\) to filter templates that appear in the **Add New Item** dialog box.  
  
|Visual C++ Value|Meaning|  
|------------------------|-------------|  
|VC-Native|Used for native projects. Also the default if a project type can't be determined.|  
|VC-Managed|Used for managed (/clr) projects|  
|VC-Windows|Used for all projects that target the windows platform (native/managed/store)|  
|WinRT-Native-UAP|Used for Windows 10 store projects|  
|CodeSharing-Native|Used for Shared item projects|  
|WinRT-Native-6.3|Used for Windows 8.1 Store projects|  
|WinRT-Native-Phone-6.3|Used for Windows Phone 8.1 projects|  
|WinRT-Native|Used for Windows 8.0 Store projects|  
|VC-Android|Used for Android projects|  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)