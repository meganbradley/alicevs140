---
title: "-OUT (Output File Name)"
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
H1: /OUT (Output File Name)
ms.assetid: 976210a4-e51f-4cfb-af5e-c16344455834
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -OUT (Output File Name)
```  
/OUT:filename  
```  
  
## Remarks  
 where:  
  
 *filename*  
 A user-specified name for the output file. It replaces the default name.  
  
## Remarks  
 The /OUT option overrides the default name and location of the program that the linker creates.  
  
 By default, the linker forms the file name using the base name of the first .obj file specified and the appropriate extension (.exe or .dll).  
  
 This option the default base name for a .mapfile or import library. For details, see [Generate Mapfile](../vs140/-MAP--Generate-Mapfile-.md) (/MAP) and [/IMPLIB](../vs140/-IMPLIB--Name-Import-Library-.md).  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **General** property page.  
  
4.  Modify the **Output File** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.OutputFile?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)