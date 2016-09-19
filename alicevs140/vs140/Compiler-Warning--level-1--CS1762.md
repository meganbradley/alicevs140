---
title: "Compiler Warning (level 1) CS1762"
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
ms.topic: error-reference
ms.assetid: 181d9063-e8a1-413d-8f0d-d05018642136
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1762
A reference was created to embedded interop assembly '<assembly1\>' because of an indirect reference to that assembly from assembly '<assembly2\>'. Consider changing the 'Embed Interop Types' property on either assembly.  
  
 You have added a reference to an assembly (assembly1) that has the `Embed Interop Types` property set to `True`. This instructs the compiler to embed interop type information from that assembly. However, the compiler cannot embed interop type information from that assembly because another assembly that you have referenced (assembly2) also references that assembly (assembly1) and has the `Embed Interop Types` property set to `False`.  
  
> [!NOTE]
>  Setting the `Embed Interop Types` property on an assembly reference to `True` is equivalent to referencing the assembly by using the `/link` option for the command-line compiler.  
  
### To address this warning  
  
-   To embed interop type information for both assemblies, set the `Embed Interop Types` property on all references to assembly1 to `True`. For more information about how to set that property, see [Walkthrough: Embedding Types from Managed Assemblies (C# and Visual Basic)](../vs140/Walkthrough--Embedding-Types-from-Managed-Assemblies--C#-and-Visual-Basic-.md).  
  
-   To remove the warning, you can set the `Embed Interop Types` property of assembly1 to `False`. In this case, a primary interop assembly (PIA) provides interop type information.  
  
## See Also  
 [/link (C# Compiler Options)](../Topic/-link%20\(C%23%20Compiler%20Options\).md)   
 [Programming with Primary Interop Assemblies](assetId:///306fa1d6-0703-4004-9e93-d0a57f1be81e)