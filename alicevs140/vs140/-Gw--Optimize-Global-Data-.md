---
title: "-Gw (Optimize Global Data)"
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
H1: /Gw (Optimize Global Data)
ms.assetid: 6f90f4e9-5eb8-4c47-886e-631278a5a4a9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Gw (Optimize Global Data)
Package global data in COMDAT sections for optimization.  
  
## Syntax  
  
```  
/Gw[-]  
```  
  
## Remarks  
 The **/Gw** option causes the compiler to package global data in individual COMDAT sections. By default, **/Gw** is off and must be explicitly enabled. To explicitly disable it, use **/Gw-**. When both **/Gw** and [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) are enabled, the linker uses whole-program optimization to compare COMDAT sections across multiple object files in order to exclude unreferenced global data or to merge identical read-only global data. This can significantly reduce the size of the resulting binary executable.  
  
 When you compile and link separately, you can use the [/OPT:REF](../Topic/-OPT%20\(Optimizations\).md) linker option to exclude from the executable the unreferenced global data in object files compiled with the **/Gw** option.  
  
 You can also use the [/OPT:ICF](../Topic/-OPT%20\(Optimizations\).md) and [/LTCG](../vs140/-LTCG--Link-time-Code-Generation-.md) linker options together to merge in the executable any identical read-only global data across multiple object files compiled with the **/Gw** option.  
  
 For more information, see [Introducing /Gw Compiler Switch](http://blogs.msdn.com/b/vcblog/archive/2013/09/11/introducing-gw-compiler-switch.aspx) on the Visual C++ Team Blog.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **C/C++** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Modify the **Additional Options** property to include **/Gw** and then choose **OK**.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)