---
title: "ProjectExtensions Element (MSBuild)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f95f312f-ff92-41eb-9469-ad99e236a307
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ProjectExtensions Element (MSBuild)
Allows [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project files to contain non-[!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] information. Anything inside of a `ProjectExtensions` element will be ignored by [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)].  
  
 <Project\>  
 <ProjectExtensions\>  
  
## Syntax  
  
```  
<ProjectExtensions>  
    Non-MSBuild information to include in file.  
</ProjectExtensions>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Project](../vs140/Project-Element--MSBuild-.md)|Required root element of an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project file.|  
  
## Remarks  
 Only one `ProjectExtensions` element may be used in an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project.  
  
## Example  
 The following code example shows information from the integrated development environment being stored in a `ProjectExtensions` element.  
  
```  
<ProjectExtensions>  
    <VSIDE>  
        <External>  
            <!--  
            Raw XML passed to the IDE by an external source  
            -->  
        </External>  
    </VSIDE>  
</ProjectExtensions>  
```  
  
## See Also  
 [MSBuild Project File Schema Reference](../vs140/MSBuild-Project-File-Schema-Reference.md)   
 [MSBuild](../Topic/MSBuild.md)