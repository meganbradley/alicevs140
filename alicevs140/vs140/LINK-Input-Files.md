---
title: "LINK Input Files"
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
ms.assetid: bb26fcc5-509a-4620-bc3e-b6c6e603a412
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# LINK Input Files
You provide the linker with files that contain objects, import and standard libraries, resources, module definitions, and command input. LINK does not use file extensions to make assumptions about the contents of a file. Instead, LINK examines each input file to determine what kind of file it is.  
  
 Object files on the command line are processed in the order they appear on the command line. Libraries are searched in command line order as well, with the following caveat: Symbols that are unresolved when bringing in an object file from a library are searched for in that library first, and then the following libraries from the command line and [/DEFAULTLIB (Specify Default Library)](../vs140/-DEFAULTLIB--Specify-Default-Library-.md) directives, and then to any libraries at the beginning of the command line.  
  
> [!NOTE]
>  LINK no longer accepts a semicolon (or any other character) as the start of a comment in response files and order files. Semicolons are recognized only as the start of comments in module-definition files (.def).  
  
 LINK uses the following types of input files:  
  
-   [.obj files](../vs140/.Obj-Files-as-Linker-Input.md)  
  
-   [.netmodule files](../vs140/.netmodule-Files-as-Linker-Input.md)  
  
-   [.lib files](../vs140/.Lib-Files-as-Linker-Input.md)  
  
-   [.exp files](../vs140/.Exp-Files-as-Linker-Input.md)  
  
-   [.def files](../vs140/.Def-Files-as-Linker-Input.md)  
  
-   [.pdb files](../vs140/.Pdb-Files-as-Linker-Input.md)  
  
-   [.res files](../vs140/.Res-Files-as-Linker-Input.md)  
  
-   [.exe files](../vs140/.Exe-Files-as-Linker-Input.md)  
  
-   [.txt files](../vs140/.Txt-Files-as-Linker-Input.md)  
  
-   [.ilk files](../vs140/.Ilk-Files-as-Linker-Input.md)  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)