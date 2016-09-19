---
title: "-Zo (Enhance Optimized Debugging)"
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
H1: /Zo (Enhance Optimized Debugging)
ms.assetid: eea8d89a-7fe0-4fe1-86b2-7689bbebbd7f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Zo (Enhance Optimized Debugging)
Generate enhanced debugging information for optimized code in non-debug builds.  
  
## Syntax  
  
```cpp  
/Zo[-]  
```  
  
## Remarks  
 The **/Zo** compiler switch generates enhanced debugging information for optimized code. Optimization may use registers for local variables, reorder code, vectorize loops, and inline function calls. These optimizations can obscure the relationship between the source code and the compiled object code. The **/Zo** switch tells the compiler to generate additional debugging information for local variables and inlined functions. Use it to see variables in the **Autos**, **Locals**, and **Watch** windows when you step through optimized code in the Visual Studio debugger. It also enables stack traces to show inlined functions in the WinDBG debugger. Debug builds that have disabled optimizations ([/Od](../Topic/-Od%20\(Disable%20\(Debug\)\).md)) do not need the additional debugging information generated when **/Zo** is specified. Use the **/Zo** switch to debug Release configurations with optimization turned on. For more information on optimization switches, see [/O Options](../vs140/-O-Options--Optimize-Code-.md). The **/Zo** option is enabled by default in Visual Studio 2015 when you specify debugging information with **/Zi** or **/Z7**. Specify **/Zo-** to explicitly disable this compiler option.  
  
 The **/Zo** switch is available in Visual Studio 2013 Update 3, and it replaces the previously undocumented **/d2Zi+** switch.  
  
### To set the /Zo compiler option in Visual Studio  
  
1.  Open the **Property Pages** dialog box for the project. For more information, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Select the **Configuration Properties**, **C/C++** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Modify the **Additional Options** property to include `/Zo` and then choose **OK**.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [/O Options (Optimize Code)](../vs140/-O-Options--Optimize-Code-.md)   
 [/Z7, /Zi, /ZI (Debug Information Format)](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md)   
 [Edit and Continue](../vs140/Edit-and-Continue.md)