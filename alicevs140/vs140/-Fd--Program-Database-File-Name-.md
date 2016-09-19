---
title: "-Fd (Program Database File Name)"
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
H1: /Fd (Program Database File Name)
ms.assetid: 3977a9ed-f0ac-45df-bf06-01cedd2ba85a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Fd (Program Database File Name)
Specifies a file name for the program database (PDB) file created by [/Z7, /Zi, /ZI (Debug Information Format)](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md).  
  
## Syntax  
  
```  
/Fdpathname  
```  
  
## Remarks  
 Without **/Fd**, the PDB file name defaults to VC`x`0.pdb., where `x` is the major version of Visual C++ in use.  
  
 If you specify a path name that does not include a file name (the path ends in backslash), the compiler creates a .pdb file named VC`x`0.pdb. in the specified directory.  
  
 If you specify a file name that does not include an extension, the compiler uses .pdb as the extension.  
  
 This option also names the state (.idb) file used for minimal rebuild and incremental compilation.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **C/C++** folder.  
  
3.  Click the **Output Files** property page.  
  
4.  Modify the **Program Database File Name** property.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ProgramDataBaseFileName?qualifyHint=False>.  
  
## Example  
 This command line creates a .pdb file named PROG.pdb and an .idb file named PROG.idb:  
  
```  
CL /DDEBUG /Zi /FdPROG.PDB PROG.CPP  
```  
  
## See Also  
 [Output-File (/F) Options](../vs140/Output-File---F--Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [Specifying the Pathname](../vs140/Specifying-the-Pathname.md)