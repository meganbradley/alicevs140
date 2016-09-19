---
title: "-DEFAULTLIB (Specify Default Library)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: /DEFAULTLIB (Specify Default Library)
ms.assetid: 6af7ff49-c170-4a13-97e2-2b9ae2de20c9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -DEFAULTLIB (Specify Default Library)
```  
/DEFAULTLIB:library  
```  
  
## Remarks  
 where:  
  
 *library*  
 The name of a library to search when resolving external references.  
  
## Remarks  
 The /DEFAULTLIB option adds one *library* to the list of libraries that LINK searches when resolving references. A library specified with /DEFAULTLIB is searched after libraries specified on the command line and before default libraries named in .obj files.  
  
 The [Ignore All Default Libraries](../vs140/-NODEFAULTLIB--Ignore-Libraries-.md) (/NODEFAULTLIB) option overrides /DEFAULTLIB:*library*. The [Ignore Libraries](../vs140/-NODEFAULTLIB--Ignore-Libraries-.md) (/NODEFAULTLIB:*library*) option overrides /DEFAULTLIB:*library* when the same *library* name is specified in both.  
  
### To set this linker option in the Visual Studio development environment  
  
-   This linker option is not available from the Visual Studio development environment. To add a library to the link phase, use the **Additional Dependencies** property from the **Input** property page.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)