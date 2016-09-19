---
title: "Compiler-Controlled LINK Options"
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
ms.assetid: e4c03896-c99c-4599-8502-e0f4bebe69d0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler-Controlled LINK Options
The CL compiler automatically calls LINK unless you specify the /c option. CL provides some control over the linker through command-line options and arguments. The following table summarizes the features in CL that affect linking.  
  
|CL specification|CL action that affects LINK|  
|----------------------|---------------------------------|  
|Any file name extension other than .c, .cxx, .cpp, or .def|Passes a file name as input to LINK|  
|*filename*.def|Passes /DEF:*filename*.def|  
|/F`number`|Passes /STACK:`number`|  
|/Fd*filename*|Passes /PDB:*filename*|  
|/Fe*filename*|Passes /OUT:*filename*|  
|/Fm*filename*|Passes /MAP:*filename*|  
|/Gy|Creates packaged functions (COMDATs); enables function-level linking|  
|/LD|Passes /DLL|  
|/LDd|Passes /DLL|  
|/link|Passes remainder of command line to LINK|  
|/MD or /MT|Places a default library name in the .obj file|  
|/MDd or /MTd|Places a default library name in the .obj file. Defines the symbol **_DEBUG**|  
|/nologo|Passes /NOLOGO|  
|/Zd|Passes /DEBUG|  
|/Zi or /Z7|Passes /DEBUG|  
|/Zl|Omits default library name from .obj file|  
  
 For more information, see [Compiler Options](../vs140/Compiler-Options.md).  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)