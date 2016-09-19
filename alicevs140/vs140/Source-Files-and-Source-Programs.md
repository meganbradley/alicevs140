---
title: "Source Files and Source Programs"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 18bb2826-17da-48e5-92a2-10e649f1bc9f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Source Files and Source Programs
A source program can be divided into one or more "source files," or "translation units." The input to the compiler is called a "translation unit."  
  
## Syntax  
 *translation-unit*:  
 *external-declaration*  
  
 *translation-unit external-declaration*  
  
 *external-declaration*:  
 *function-definition*  
  
 *declaration*  
  
 [Overview of Declarations](../vs140/Overview-of-Declarations.md) gives the syntax for the `declaration` nonterminal, and the *Preprocessor Reference* explains how the [translation unit](../vs140/Phases-of-Translation.md) is processed.  
  
> [!NOTE]
>  See the introduction to [C Language Syntax Summary](../vs140/C-Language-Syntax-Summary.md), for an explanation of the ANSI syntax conventions.  
  
 The components of a translation unit are external declarations that include function definitions and identifier declarations. These declarations and definitions can be in source files, header files, libraries, and other files the program needs. You must compile each translation unit and link the resulting object files to make a program.  
  
 A C "source program" is a collection of directives, pragmas, declarations, definitions, statement blocks, and functions. To be valid components of a Microsoft C program, each must have the syntax described in this book, although they can appear in any order in the program (subject to the rules outlined throughout this book). However, the location of these components in a program does affect how variables and functions can be used in a program. (See [Lifetime, Scope, Visibility, and Linkage](../vs140/Lifetime--Scope--Visibility--and-Linkage.md) for more information.)  
  
 Source files need not contain executable statements. For example, you may find it useful to place definitions of variables in one source file and then declare references to these variables in other source files that use them. This technique makes the definitions easy to find and update when necessary. For the same reason, constants and macros are often organized into separate files called "include files" or "header files" that can be referenced in source files as required. See the *Preprocessor Reference* for information about [macros](../vs140/Macros--C-C---.md) and [include files](../vs140/#include-Directive--C-C---.md).  
  
## See Also  
 [Program Structure](../vs140/Program-Structure.md)