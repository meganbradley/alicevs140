---
title: "Neutral Resources Languages for Localization"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef064995-3b84-4698-a708-9689b7723533
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Neutral Resources Languages for Localization
The <xref:System.Resources.NeutralResourcesLanguageAttribute?qualifyHint=False> class specifies the culture of the resources included in the main assembly. This attribute is used as a performance enhancement, so that the <xref:System.Resources.ResourceManager?qualifyHint=False> object does not search for resources that are included in the main assembly.  
  
 The following code shows how to set the neutral resources language. The code can be placed in either a build script or in the AssemblyInfo.vb or AssemblyInfo.cs file.  
  
```vb#  
' Set neutral resources language for assembly.  
<Assembly: NeutralResourcesLanguageAttribute("en")>  
  
```  
  
```c#  
// Set neutral resources language for assembly.  
[assembly: NeutralResourcesLanguageAttribute("en")]  
```  
  
## See Also  
 <xref:System.Resources.ResourceManager?qualifyHint=False>   
 [Introduction to International Applications Based on the .NET Framework](../vs140/Introduction-to-International-Applications-Based-on-the-.NET-Framework.md)   
 [Hierarchical Organization of Resources for Localization](../vs140/Hierarchical-Organization-of-Resources-for-Localization.md)   
 [Localizing Applications](../vs140/Localizing-Applications.md)   
 [Globalizing and Localizing Applications](../Topic/Globalizing%20and%20Localizing%20Applications.md)