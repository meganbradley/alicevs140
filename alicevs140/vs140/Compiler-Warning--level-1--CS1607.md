---
title: "Compiler Warning (level 1) CS1607"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 7ad8e1a4-40c2-41cc-b4ee-cc4d7beb4372
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1607
Assembly generation -- reason  
  
 A warning was generated from the assembly-creation phase of the compilation.  
  
 If you are building a 64-bit application on a 32-bit operating system, you must ensure that 64-bit versions of all referenced assemblies are installed on the target operating system.  
  
 All x86-specific common language runtime (CLR) assemblies have 64-bit counterparts (every CLR assembly will exist on all operating systems). Therefore, you can safely ignore CS1607 for CLR assemblies.  
  
 You can ignore this warning if you encounter it when you create a <xref:System.Reflection.AssemblyInformationalVersionAttribute?qualifyHint=False>. The informational version is a string that attaches additional version information to an assembly; this information is not used at run time. Although you can specify any text, a warning message appears on compilation if the string is not in the format that is used by the assembly version number, or if it is in that format but contains wildcard characters. This warning is harmless.  
  
 For more information, see [Al.exe Tool Errors and Warnings](assetId:///7f125d49-0a03-47a6-9ba9-d61a679a7d4b).