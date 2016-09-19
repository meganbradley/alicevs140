---
title: "-target:module (C# Compiler Options)"
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
H1: /target:module (C# Compiler Options)
ms.assetid: 9af1e4fa-c749-44e7-ae58-90a3d05d4e72
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -target:module (C# Compiler Options)
This option causes the compiler to not generate an assembly manifest.  
  
## Syntax  
  
```  
/target:module  
```  
  
## Remarks  
 By default, the output file created by compiling with this option will have an extension of .netmodule.  
  
 A file that does not have an assembly manifest cannot be loaded by the .NET Framework common language runtime. However, such a file can be incorporated into the assembly manifest of an assembly by means of [/addmodule](../Topic/-addmodule%20\(C%23%20Compiler%20Options\).md).  
  
 If more than one module is created in a single compilation, [internal](../vs140/internal--C#-Reference-.md) types in one module will be available to other modules in the compilation. When code in one module references `internal` types in another module, then both modules must be incorporated into an assembly manifest, by means of **/addmodule**.  
  
 Creating a module is not supported in the Visual Studio development environment.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.ProjectProperties3.OutputType?qualifyHint=False>.  
  
## Example  
 Compile `in.cs`, creating `in.netmodule`:  
  
```  
csc /target:module in.cs  
```  
  
## See Also  
 [/target (C# Compiler Options)](../Topic/-target%20\(C%23%20Compiler%20Options\).md)   
 [C# Compiler Options](../vs140/C#-Compiler-Options.md)