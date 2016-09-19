---
title: "-moduleassemblyname"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
H1: /moduleassemblyname
ms.assetid: 013a57b6-f425-4dd3-b333-512d72c42f55
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -moduleassemblyname
Specifies the name of the assembly that this module will be a part of.  
  
## Syntax  
  
```  
/moduleassemblyname:assembly_name  
```  
  
## Arguments  
  
|||  
|-|-|  
|Term|Definition|  
|`assembly_name`|The name of the assembly that this module will be a part of.|  
  
## Remarks  
 The compiler processes the `/moduleassemblyname` option only if the `/target:module` option has been specified. This causes the compiler to create a module. The module created by the compiler is valid only for the assembly specified with the `/moduleassemblyname` option. If you place the module in a different assembly, run-time errors will occur.  
  
 The `/moduleassemblyname` option is needed only when the following are true:  
  
-   A data type in the module needs access to a `Friend` type in a referenced assembly.  
  
-   The referenced assembly has granted friend assembly access to the assembly into which the module will be built.  
  
 For more information about creating a module, see [/target (Visual Basic)](../Topic/-target%20\(Visual%20Basic\).md). For more information about friend assemblies, see [Friend Assemblies (C# and Visual Basic)](../vs140/Friend-Assemblies--C#-and-Visual-Basic-.md).  
  
> [!NOTE]
>  The `/moduleassemblyname` option is not available from within the Visual Studio development environment; it is available only when you compile from a command prompt.  
  
## See Also  
 [How to: Build a Multifile Assembly](assetId:///261c5583-8a76-412d-bda7-9b8ee3b131e5)   
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [/target (Visual Basic)](../Topic/-target%20\(Visual%20Basic\).md)   
 [/main](../Topic/-main.md)   
 [/reference (Visual Basic)](../vs140/-reference--Visual-Basic-.md)   
 [/addmodule](../vs140/-addmodule.md)   
 [Assemblies and the Global Assembly Cache (C# and Visual Basic)](../vs140/Assemblies-and-the-Global-Assembly-Cache--C#-and-Visual-Basic-.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [Friend Assemblies (C# and Visual Basic)](../vs140/Friend-Assemblies--C#-and-Visual-Basic-.md)