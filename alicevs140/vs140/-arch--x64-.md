---
title: "-arch (x64)"
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
H1: /arch (x64)
ms.assetid: ecda22bf-5bed-43f4-99fb-88aedd83d9d8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -arch (x64)
Specifies the architecture for code generation on x64. Also see [/arch (x86)](../vs140/-arch--x86-.md) and [/arch (ARM)](../Topic/-arch%20\(ARM\).md).  
  
## Syntax  
  
```  
/arch:[AVX|AVX2]  
```  
  
## Arguments  
 **/arch:AVX**  
 Enables the use of Intel Advanced Vector Extensions instructions.  
  
 **/arch:AVX2**  
 Enables the use of Intel Advanced Vector Extensions 2 instructions.  
  
## Remarks  
 **/arch** only affects code generation for native functions. When you use [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) to compile, **/arch** has no effect on code generation for managed functions.  
  
 The `__AVX__` preprocessor symbol is defined when the **/arch:AVX** compiler option is specified. The `__AVX2__` preprocessor symbol is defined when the **/arch:AVX2** compiler option is specified. For more information, see [Predefined Macros](../vs140/Predefined-Macros.md). The **/arch:AVX2** option was introduced in Visual Studio 2013 Update 2, version 12.0.34567.1.  
  
### To set the /arch:AVX or /arch:AVX2 compiler option in Visual Studio  
  
1.  Open the **Property Pages** dialog box for the project. For more information, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Select the **Configuration Properties**, **C/C++** folder.  
  
3.  Select the **Code Generation** property page.  
  
4.  In the **Enable Enhanced Instruction Set** drop-down box, choose **Advanced Vector Extensions (/arch:AVX)** or **Advanced Vector Extensions 2 (/arch:AVX2)**.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.EnableEnhancedInstructionSet?qualifyHint=False>.  
  
## See Also  
 [/arch (Minimum CPU Architecture)](../vs140/-arch--Minimum-CPU-Architecture-.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)