---
title: "-Ox (Full Optimization)"
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
H1: /Ox (Full Optimization)
ms.assetid: 3ad7c30b-c615-428c-b1d0-2e024f81c760
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Ox (Full Optimization)
The **/Ox** compiler option produces code that favors execution speed over smaller size.  
  
## Syntax  
  
```  
/Ox  
```  
  
## Remarks  
 Specifying the **/Ox** compiler option is the same as using the following options:  
  
-   [/Ob (Inline Function Expansion)](../Topic/-Ob%20\(Inline%20Function%20Expansion\).md), where the option parameter is 2 (**/Ob2**)  
  
-   [/Og (Global Optimizations)](../vs140/-Og--Global-Optimizations-.md)  
  
-   [/Oi (Generate Intrinsic Functions)](../vs140/-Oi--Generate-Intrinsic-Functions-.md)  
  
-   [/Ot (Favor Fast Code)](../vs140/-Os---Ot--Favor-Small-Code--Favor-Fast-Code-.md)  
  
-   [/Oy (Frame-Pointer Omission)](../Topic/-Oy%20\(Frame-Pointer%20Omission\).md)  
  
 **/Ox** is mutually exclusive from:  
  
-   [/O1 (Minimize Size)](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md)  
  
-   [/O2 (Maximize Speed)](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md)  
  
-   [/Od (Disable (Debug))](../Topic/-Od%20\(Disable%20\(Debug\)\).md)  
  
 The **/Ox** compiler option also enables the Named Return Value optimization, which eliminates the copy constructor and destructor of a stack based return value. For more information, see [/O1, /O2 (Minimize Size, Maximize Speed)](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md).  
  
 You can cancel out the **/Ox** compiler option if you specify **/Oxs**, which combines the **/Ox** compiler option with [/Os (Favor Small Code)](../vs140/-Os---Ot--Favor-Small-Code--Favor-Fast-Code-.md). The combined options favor smaller code size.  
  
 In general, specify [/O2 (Maximize Speed)](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md) instead of **/Ox**, and [/O1 (Minimize Size)](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md) instead of **/Oxs**.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **C/C++** folder.  
  
3.  Click the **Optimization** property page.  
  
4.  Modify the **Optimization** property.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.Optimization?qualifyHint=False>.  
  
## See Also  
 [/O Options (Optimize Code)](../vs140/-O-Options--Optimize-Code-.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)