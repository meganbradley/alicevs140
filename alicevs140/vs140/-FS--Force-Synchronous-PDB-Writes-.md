---
title: "-FS (Force Synchronous PDB Writes)"
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
H1: /FS (Force Synchronous PDB Writes)
ms.assetid: b2caaffe-f6e1-4963-b068-648f06b105e0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -FS (Force Synchronous PDB Writes)
Forces writes to the program database (PDB) file—created by [/Zi](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md) or [/ZI](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md)—to be serialized through MSPDBSRV.EXE.  
  
## Syntax  
  
```  
/FS  
```  
  
## Remarks  
 By default, when **/Zi** or **/ZI** is specified, the compiler locks PDB files to write type information and symbolic debugging information. This can significantly reduce the time it takes the compiler to generate type information when the number of types is large. If another process temporarily locks the PDB file—for example, an anti-virus program—writes by the compiler may fail and a fatal error may occur. This problem can also happen when multiple copies of cl.exe access the same PDB file—for example, if your solution has independent projects that use the same intermediate directories or output directories and parallel builds are enabled. The **/FS** compiler option prevents the compiler from locking the PDB file and forces writes to go through MSPDBSRV.EXE, which serializes access. This may make builds significantly longer, and it doesn't prevent all errors that may occur when multiple instances of cl.exe access the PDB file at the same time. We recommend that you change your solution so that independent projects write to separate intermediate and output locations, or that you make one of the projects dependent on the other to force serialized project builds.  
  
 The [/MP](../vs140/-MP--Build-with-Multiple-Processes-.md) option enables **/FS** by default.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **C/C++** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Modify the **Additional Options** property to include `/FS` and then choose **OK**.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)