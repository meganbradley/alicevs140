---
title: "-U, -u (Undefine Symbols)"
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
H1: /U, /u (Undefine Symbols)
ms.assetid: 7bc0474f-6d1f-419b-807d-0d8816763b2a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -U, -u (Undefine Symbols)
The **/U** compiler option undefines the specified preprocessor symbol. The **/u** compiler option undefines the Microsoft-specific symbols that the compiler defines.  
  
## Syntax  
  
```  
/U[ ]symbol  
/u  
```  
  
## Arguments  
 `symbol`  
 The preprocessor symbol to undefine.  
  
## Remarks  
 Neither the **/U** or **/u** option can undefine a symbol created by using the **#define** directive.  
  
 The **/U** option can undefine a symbol that was previously defined by using the **/D** option.  
  
 By default, the compiler defines the following Microsoft-specific symbols.  
  
|Symbol|Function|  
|------------|--------------|  
|_CHAR_UNSIGNED|Default char type is unsigned. Defined when the [/J](../vs140/-J--Default-char-Type-Is-unsigned-.md) option is specified.|  
|_CPPRTTI|Defined for code compiled with the [/GR](../Topic/-GR%20\(Enable%20Run-Time%20Type%20Information\).md) option.|  
|_CPPUNWIND|Defined for code compiled with the [/EHsc](../vs140/-EH--Exception-Handling-Model-.md) option.|  
|_DLL|Defined when the [/MD](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md) option is specified.|  
|_M_IX86|By default, defined to 600 for x86 targets.|  
|_MSC_VER|For more information, see [Predefined Macros](../vs140/Predefined-Macros.md).|  
|_WIN32|Defined for WIN32 applications. Always defined.|  
|_MT|Defined when the [/MD or /MT](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md) option is specified.|  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Click the **C/C++** folder.  
  
3.  Click the **Advanced** property page.  
  
4.  Modify the **Undefine Preprocessor Definitions** or **Undefine All Preprocessor Definitions** properties.  
  
### To set this compiler option programmatically  
  
-   See <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UndefineAllPreprocessorDefinitions?qualifyHint=False> or <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UndefinePreprocessorDefinitions?qualifyHint=False>.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)   
 [/J (Default char Type Is unsigned)](../vs140/-J--Default-char-Type-Is-unsigned-.md)   
 [/GR (Enable Run-Time Type Information)](../Topic/-GR%20\(Enable%20Run-Time%20Type%20Information\).md)   
 [/EH (Exception Handling Model)](../vs140/-EH--Exception-Handling-Model-.md)   
 [/MD, /MT, /LD (Use Run-Time Library)](../Topic/-MD,%20-MT,%20-LD%20\(Use%20Run-Time%20Library\).md)