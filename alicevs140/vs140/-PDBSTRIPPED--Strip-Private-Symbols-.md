---
title: "-PDBSTRIPPED (Strip Private Symbols)"
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
H1: /PDBSTRIPPED (Strip Private Symbols)
ms.assetid: 9b9e0070-6a13-4142-8180-19c003fbbd55
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -PDBSTRIPPED (Strip Private Symbols)
```  
/PDBSTRIPPED:pdb_file_name  
```  
  
## Remarks  
 where:  
  
 *pdb_file_name*  
 A user-specified name for the stripped program database (PDB) that the linker creates.  
  
## Remarks  
 The /PDBSTRIPPED option creates a second program database (PDB) file when you build your program image with any of the compiler or linker options that generate a PDB file ([/DEBUG](../Topic/-DEBUG%20\(Generate%20Debug%20Info\).md), [/Z7](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md), /Zd, or /Zi). This second PDB file omits symbols that you would not want to ship to your customers. The second PDB file will only contain:  
  
-   Public symbols  
  
-   The list of object files and the portions of the executable to which they contribute  
  
-   Frame pointer optimization (FPO) debug records used to traverse the stack  
  
 The stripped PDB file will not contain:  
  
-   Type information  
  
-   Line number information  
  
-   Per-object file CodeView symbols such as those for functions, locals, and static data  
  
 The full PDB file will still be generated when you use /PDBSTRIPPED.  
  
 If you do not create a PDB file, /PDBSTRIPPED is ignored.  
  
### To set this linker option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Setting Visual C++ Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **Debug** property page.  
  
4.  Modify the **Strip Private Symbols** property.  
  
### To set this linker option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.StripPrivateSymbols?qualifyHint=False>.  
  
## See Also  
 [Setting Linker Options](../vs140/Setting-Linker-Options.md)   
 [Linker Options](../Topic/Linker%20Options.md)