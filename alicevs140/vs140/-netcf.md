---
title: "-netcf"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
H1: /netcf
ms.assetid: db7cfa59-c315-401c-a59b-0daf355343d6
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -netcf
Sets the compiler to target the [!INCLUDE[Compact](../vs140/includes/compact_md.md)].  
  
## Syntax  
  
```  
/netcf  
```  
  
## Remarks  
 The `/netcf` option causes the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler to target the [!INCLUDE[Compact](../vs140/includes/compact_md.md)] rather than the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]. Language functionality that is present only in the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] is disabled.  
  
 The `/netcf` option is designed to be used with [/sdkpath](../vs140/-sdkpath.md). The language features disabled by `/netcf` are the same language features not present in the files targeted with `/sdkpath`.  
  
> [!NOTE]
>  The `/netcf` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line. The `/netcf` option is set when a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] device project is loaded.  
  
 The `/netcf` option changes the following language features:  
  
-   The [End <keyword\> Statement](../vs140/End--keyword--Statement--Visual-Basic-.md) keyword, which terminates execution of a program, is disabled. The following program compiles and runs without `/netcf` but fails at compile time with `/netcf`.  
  
     [!CODE [VbVbalrCompiler#34](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#34)]  
  
-   Late binding, in all forms, is disabled. Compile-time errors are generated when recognized late-binding scenarios are encountered. The following program compiles and runs without `/netcf` but fails at compile time with `/netcf`.  
  
     [!CODE [VbVbalrCompiler#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#35)]  
  
-   The [Auto](../vs140/Auto--Visual-Basic-.md), [Ansi](../vs140/Ansi--Visual-Basic-.md), and [Unicode](../vs140/Unicode--Visual-Basic-.md) modifiers are disabled. The syntax of the [Declare Statement](../Topic/Declare%20Statement.md) statement is also modified to `Declare Sub|Function name Lib "library" [Alias "alias"] [([arglist])]`. The following code shows the effect of `/netcf` on a compilation.  
  
     [!CODE [VbVbalrCompiler#36](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#36)]  
  
-   Using Visual Basic 6.0 keywords that were removed from [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] generates a different error when `/netcf` is used. This affects the error messages for the following keywords:  
  
    -   `Open`  
  
    -   `Close`  
  
    -   `Put`  
  
    -   `Print`  
  
    -   `Write`  
  
    -   `Input`  
  
    -   `Lock`  
  
    -   `Unlock`  
  
    -   `Seek`  
  
    -   `Width`  
  
    -   `Name`  
  
    -   `FreeFile`  
  
    -   `EOF`  
  
    -   `Loc`  
  
    -   `LOF`  
  
    -   `Line`  
  
## Example  
 The following code compiles `Myfile.vb` with the [!INCLUDE[Compact](../vs140/includes/compact_md.md)], using the versions of Mscorlib.dll and Microsoft.VisualBasic.dll found in the default installation directory of the [!INCLUDE[Compact](../vs140/includes/compact_md.md)] on the C drive. Typically, you would use the most recent version of the [!INCLUDE[Compact](../vs140/includes/compact_md.md)].  
  
```  
vbc /netcf /sdkpath:"c:\Program Files\Microsoft Visual Studio .NET 2003\CompactFrameworkSDK\v1.0.5000\Windows CE " myfile.vb  
```  
  
## See Also  
 [Visual Basic Command-Line Compiler](../vs140/Visual-Basic-Command-Line-Compiler.md)   
 [Sample Compilation Command Lines](../vs140/Sample-Compilation-Command-Lines--Visual-Basic-.md)   
 [/sdkpath](../vs140/-sdkpath.md)