---
title: "-target:library (C# Compiler Options)"
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
H1: /target:library (C# Compiler Options)
ms.assetid: c5670e88-2126-47c1-8d1c-217923837d17
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -target:library (C# Compiler Options)
The **/target:library** option causes the compiler to create a dynamic-link library (DLL) rather than an executable file (EXE).  
  
## Syntax  
  
```  
/target:library  
```  
  
## Remarks  
 The DLL will be created with the .dll extension.  
  
 Unless otherwise specified with the [/out](../Topic/-out%20\(C%23%20Compiler%20Options\).md) option, the output file name takes the name of the first input file.  
  
 When specified at the command line, all files up to the next **/out** or **/target:module** option are used to create the .dll file.  
  
 When building a .dll file, a [Main](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md) method is not required.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** page.  
  
2.  Click the **Application** property page.  
  
3.  Modify the **Output type** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.OutputType?qualifyHint=False>.  
  
## Example  
 Compile `in.cs`, creating `in.dll`:  
  
```  
csc /target:library in.cs  
```  
  
## See Also  
 [/target (C# Compiler Options)](../Topic/-target%20\(C%23%20Compiler%20Options\).md)   
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)