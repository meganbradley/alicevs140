---
title: "-target:exe (C# Compiler Options)"
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
H1: /target:exe (C# Compiler Options)
ms.assetid: bda5717d-1b91-4848-956b-fcf85c30e432
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -target:exe (C# Compiler Options)
The **/target:exe** option causes the compiler to create an executable (EXE), console application.  
  
## Syntax  
  
```  
/target:exe  
```  
  
## Remarks  
 The **/target:exe** option is in effect by default. The executable file will be created with the .exe extension.  
  
 Use [/target:winexe](../Topic/-target:winexe%20\(C%23%20Compiler%20Options\).md) to create a Windows program executable.  
  
 Unless otherwise specified with the [/out](../Topic/-out%20\(C%23%20Compiler%20Options\).md) option, the output file name takes the name of the input file that contains the [Main](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md) method.  
  
 When specified at the command line, all files up to the next **/out** or **/target:module** option are used to create the .exe file  
  
 One and only one **Main** method is required in the source code files that are compiled into an .exe file. The [/main](../Topic/-main%20\(C%23%20Compiler%20Options\).md) compiler option lets you specify which class contains the **Main** method, in cases where your code has more than one class with a **Main** method.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** page.  
  
2.  Click the **Application** property page.  
  
3.  Modify the **Output type** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.OutputType?qualifyHint=False>.  
  
## Example  
 Each of the following command lines will compile `in.cs`, creating `in.exe`:  
  
```  
csc /target:exe in.cs  
csc in.cs  
```  
  
## See Also  
 [/target (C# Compiler Options)](../Topic/-target%20\(C%23%20Compiler%20Options\).md)   
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)