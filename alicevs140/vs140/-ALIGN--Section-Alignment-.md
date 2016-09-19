---
title: "-ALIGN (Section Alignment)"
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
H1: /ALIGN (Section Alignment)
ms.assetid: f2f8ac24-e90e-4bea-8205-f2960a3b1740
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -ALIGN (Section Alignment)
```  
/ALIGN[:number]  
```  
  
## Remarks  
 where:  
  
 `number`  
 The alignment value.  
  
## Remarks  
 The /ALIGN option specifies the alignment of each section within the linear address space of the program. The `number` argument is in bytes and must be a power of two. The default is 4K (4096). The linker issues a warning if the alignment produces an invalid image.  
  
 Unless you are writing an application such as a device driver, you should not need to modify the alignment.  
  
 It is possible to modify the alignment of a particular section with the align parameter to the [/SECTION](../vs140/-SECTION--Specify-Section-Attributes-.md) option.  
  
 The alignment value that you specify cannot be smaller than the largest section alignment.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Command Line** property page.  
  
4.  Type the option into the **Additional Options** box.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)