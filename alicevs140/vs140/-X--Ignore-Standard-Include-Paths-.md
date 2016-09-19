---
title: "-X (Ignore Standard Include Paths)"
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
H1: /X (Ignore Standard Include Paths)
ms.assetid: 16bdf2cc-c8dc-46e4-bdcc-f3caeba5e1ef
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -X (Ignore Standard Include Paths)
Prevents the compiler from searching for include files in directories specified in the PATH and INCLUDE environment variables.  
  
## Syntax  
  
```  
/X  
```  
  
## Remarks  
 You can use this option with the [/I (Additional Include Directories)](../vs140/-I--Additional-Include-Directories-.md) (**/I**`directory`) option.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **C/C++** folder.  
  
3.  Click the **Preprocessor** property page.  
  
4.  Modify the **Ignore Standard Include Path** property.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.IgnoreStandardIncludePath?qualifyHint=False>.  
  
## Example  
 In the following command, `/X` tells the compiler to ignore locations specified by the PATH and INCLUDE environment variables, and `/I` specifies the directory in which to look for include files:  
  
```  
CL /X /I \ALT\INCLUDE MAIN.C  
```  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)