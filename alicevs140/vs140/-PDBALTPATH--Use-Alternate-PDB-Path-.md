---
title: "-PDBALTPATH (Use Alternate PDB Path)"
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
H1: /PDBALTPATH (Use Alternate PDB Path)
ms.assetid: 72e200aa-e2c3-4ad8-b687-25528da1aaaf
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -PDBALTPATH (Use Alternate PDB Path)
```  
/PDBALTPATH:pdb_file_name  
```  
  
## Remarks  
 where:  
  
 *pdb_file_name*  
 The path and file name for the .pdb file.  
  
## Remarks  
 Use this option to provide an alternate location for the Program Database (.pdb) file in a compiled binary file. Normally, the linker records the location of the .pdb file in the binaries that it produces. You can use this option to provide a different path and file name for the .pdb file. The information provided with /PDBALTPATH does not change the location or name of the actual .pdb file; it changes the information that the linker writes in the binary file. This enables you to provide a path that is independent of the file structure of the build computer. Two common uses for this option are to provide a network path or a file that has no path information.  
  
 The value of *pdb_file_name* can be an arbitrary string, an environment variable, or **%_PDB%**. The linker will expand an environment variable, such as **%SystemRoot%**, to its value. The linker defines the environment variables **%_PDB%** and **%_EXT%**. **%_PDB%** expands to the file name of the actual .pdb file without any path information and **%_EXT%** is the extension of the generated executable.  
  
## See Also  
 [DUMPBIN Options](../vs140/DUMPBIN-Options.md)   
 [/PDBPATH](../vs140/-PDBPATH.md)