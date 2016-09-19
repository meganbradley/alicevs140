---
title: "-Qsafe_fp_loads"
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
H1: /Qsafe_fp_loads
ms.assetid: 2b2ce52d-ba57-4bd3-a739-47a7f8bfaba9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Qsafe_fp_loads
Requires integer move instructions for floating-point values and disables certain floating-point load optimizations.  
  
## Syntax  
  
```  
/Qsafe_fp_loads  
```  
  
## Remarks  
 **/Qsafe_fp_loads** is only available in the compilers that target x86; it is not available in the compilers that target x64 or ARM.  
  
 **/Qsafe_fp_loads** forces the compiler to use integer move instructions instead of floating-point move instructions to move data between memory and MMX registers. This option also disables register load optimization for floating-point values that can be loaded in multiple control paths when the value may cause an exception on load—for example, a NaN value.  
  
 This option is overridden by [/fp:except](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md). **/Qsafe_fp_loads** specifies a subset of the compiler behavior that's specified by **/fp:except**.  
  
 **/Qsafe_fp_loads** is incompatible with [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) and [/fp:fast](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md). For more information about floating point compiler options, see [/fp (Specify Floating-Point Behavior)](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md).  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Select the **C/C++** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Type the compiler option in the **Additional Options** box.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [/Q Options (Low-Level Operations)](../vs140/-Q-Options--Low-Level-Operations-.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)