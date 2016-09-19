---
title: "-Gm (Enable Minimal Rebuild)"
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
H1: /Gm (Enable Minimal Rebuild)
ms.assetid: d8869ce0-d2ea-40eb-8dae-6d2cdb61dd59
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Gm (Enable Minimal Rebuild)
Enables minimal rebuild, which determines whether C++ source files that include changed C++ class definitions (stored in header (.h) files) need to be recompiled.  
  
## Syntax  
  
```  
/Gm  
```  
  
## Remarks  
 The compiler stores dependency information between source files and class definitions in the project's .idb file during the first compile. (Dependency information tells which source file is dependent on which class definition, and which .h file the definition is located in.) Subsequent compiles use the information stored in the .idb file to determine whether a source file needs to be compiled, even if it includes a modified .h file.  
  
> [!NOTE]
>  Minimal rebuild relies on class definitions not changing between include files. Class definitions must be global for a project (there should be only one definition of a given class), because the dependency information in the .idb file is created for the entire project. If you have more than one definition for a class in your project, disable minimal rebuild.  
  
 Because the incremental linker does not support the Windows metadata included in .obj files by using the [/ZW](../vs140/-ZW--Windows-Runtime-Compilation-.md) option, the **/Gm** option is incompatible with **/ZW**.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **C/C++** folder.  
  
3.  Click the **Code Generation** property page.  
  
4.  Modify the **Enable Minimal Rebuild** property.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.MinimalRebuild?qualifyHint=False>.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)