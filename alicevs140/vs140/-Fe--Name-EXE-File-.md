---
title: "-Fe (Name EXE File)"
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
H1: /Fe (Name EXE File)
ms.assetid: 49f594fd-5e94-45fe-a1bf-7c9f2abb6437
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Fe (Name EXE File)
Specifies a name and a directory for the .exe file or DLL created by the compiler.  
  
## Syntax  
  
```  
/Fepathname  
```  
  
## Remarks  
 Without this option, the compiler gives the file a default name using the base name of the first source or object file specified on the command line and the extension .exe or .dll.  
  
 If you specify the[/c (Compile Without Linking)](../Topic/-c%20\(Compile%20Without%20Linking\).md), to compile without linking, **/Fe** has no effect.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **Linker** folder.  
  
3.  Click the **General**property page.  
  
4.  Modify the **Output File** property.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.OutputFile?qualifyHint=False>.  
  
## Example  
 The following command line compiles and links all C source files in the current directory. The resulting executable file is named PROCESS.exe and is created in the directory C:\BIN.  
  
```  
CL /FeC:\BIN\PROCESS *.C  
```  
  
## Example  
 The following command line creates an executable file in `C:\BIN` with the same base name as the first source or object file:  
  
```  
CL /FeC:\BIN\ *.C  
```  
  
## See Also  
 [Output-File (/F) Options](../vs140/Output-File---F--Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [Specifying the Pathname](../vs140/Specifying-the-Pathname.md)