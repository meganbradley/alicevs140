---
title: "-optimize (C# Compiler Options)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: /optimize (C# Compiler Options)
ms.assetid: 6dd5b6f2-cd1d-4593-a9f4-1c2ed9404ca0
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -optimize (C# Compiler Options)
The **/optimize** option enables or disables optimizations performed by the compiler to make your output file smaller, faster, and more efficient.  
  
## Syntax  
  
```  
/optimize[+ | -]  
```  
  
## Remarks  
 **/optimize** also tells the common language runtime to optimize code at runtime.  
  
 By default, optimizations are disabled. Specify **/optimize+** to enable optimizations.  
  
 When building a module to be used by an assembly, use the same **/optimize** settings as those of the assembly.  
  
 **/o** is the short form of **/optimize**.  
  
 It is possible to combine the **/optimize** and [/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md) options.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** page.  
  
2.  Click the **Build** property page.  
  
3.  Modify the **Optimize Code** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.Optimize?qualifyHint=False>.  
  
## Example  
 Compile `t2.cs` and enable compiler optimizations:  
  
```  
csc t2.cs /optimize  
```  
  
## See Also  
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)   
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)