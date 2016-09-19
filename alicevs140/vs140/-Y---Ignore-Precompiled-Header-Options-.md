---
title: "-Y- (Ignore Precompiled Header Options)"
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
H1: /Y- (Ignore Precompiled Header Options)
ms.assetid: cfaecb36-58db-46b8-b04d-cca6072b1b7a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Y- (Ignore Precompiled Header Options)
Causes all other `/Y` compiler options to be ignored (and cannot itself be overridden).  
  
## Syntax  
  
```  
/Y-  
```  
  
## Remarks  
 For more information on precompiled headers, see:  
  
-   [/Y (Precompiled Headers)](../vs140/-Y--Precompiled-Headers-.md)  
  
-   [Creating Precompiled Header Files](../vs140/Creating-Precompiled-Header-Files.md)  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **C/C++** folder.  
  
3.  Click the **Command Line** property page.  
  
4.  Type the compiler option in the **Additional Options** box.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions?qualifyHint=False>.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)