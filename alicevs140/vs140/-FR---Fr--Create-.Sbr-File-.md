---
title: "-FR, -Fr (Create .Sbr File)"
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
H1: /FR, /Fr (Create .Sbr File)
ms.assetid: 3fd8f88b-3924-4feb-9393-287036a28896
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -FR, -Fr (Create .Sbr File)
Creates .sbr files.  
  
## Syntax  
  
```  
/FR[pathname[\filename]]  
/Fr[pathname[\filename]]  
```  
  
## Remarks  
 During the build process, the Microsoft Browse Information File Maintenance Utility (BSCMAKE) uses these files to create a .BSC file, which is used to display browse information.  
  
 **/FR** creates an .sbr file with complete symbolic information.  
  
 **/Fr** creates an .sbr file without information on local variables.  
  
 If you do not specify `filename`, the .sbr file gets the same base name as the source file.  
  
 **/Fr** is deprecated; use **/FR** instead. For more information, see Deprecated and Removed Compiler Options in [Compiler Options Listed by Category](../vs140/Compiler-Options-Listed-by-Category.md).  
  
> [!NOTE]
>  Do not change the .sbr extension. BSCMAKE requires the intermediary files to have that extension.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  In the navigation pane, choose the **C/C++**, **Browse Information** property page.  
  
3.  Modify the **Browse Information File** or **Enable Browse Information** property.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.BrowseInformation?qualifyHint=False> and <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.BrowseInformationFile?qualifyHint=False>.  
  
## See Also  
 [Output-File (/F) Options](../vs140/Output-File---F--Options.md)   
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [Specifying the Pathname](../vs140/Specifying-the-Pathname.md)