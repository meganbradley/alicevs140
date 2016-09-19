---
title: "-GA (Optimize for Windows Application)"
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
H1: /GA (Optimize for Windows Application)
ms.assetid: be97323e-15a0-4836-862c-95980b51926a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -GA (Optimize for Windows Application)
Results in more efficient code for an .exe file for accessing thread-local storage (TLS) variables.  
  
## Syntax  
  
```  
/GA  
```  
  
## Remarks  
 **/GA** speeds access to data declared with [__declspec(thread)](../vs140/__declspec.md) in a Windows-based program. When this option is set, the [__tls_index](http://msdn.microsoft.com/library/windows/desktop/ms686749) macro is assumed to be 0.  
  
 Using **/GA** for a DLL can result in bad code generation.  
  
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