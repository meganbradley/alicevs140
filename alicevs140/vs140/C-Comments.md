---
title: "C Comments"
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
ms.assetid: 0f5f2825-e673-49e7-8669-94e2f5294989
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Comments
A "comment" is a sequence of characters beginning with a forward slash/asterisk combination (**/\***) that is treated as a single white-space character by the compiler and is otherwise ignored. A comment can include any combination of characters from the representable character set, including newline characters, but excluding the "end comment" delimiter (**\*/**). Comments can occupy more than one line but cannot be nested.  
  
 Comments can appear anywhere a white-space character is allowed. Since the compiler treats a comment as a single white-space character, you cannot include comments within tokens. The compiler ignores the characters in the comment.  
  
 Use comments to document your code. This example is a comment accepted by the compiler:  
  
```  
/* Comments can contain keywords such as  
   for and while without generating errors. */  
```  
  
 Comments can appear on the same line as a code statement:  
  
```  
printf( "Hello\n" );  /* Comments can go here */  
```  
  
 You can choose to precede functions or program modules with a descriptive comment block:  
  
```  
/* MATHERR.C illustrates writing an error routine   
 * for math functions.   
 */   
```  
  
 Since comments cannot contain nested comments, this example causes an error:  
  
```  
/* Comment out this routine for testing   
  
   /* Open file */  
    fh = _open( "myfile.c", _O_RDONLY );  
    .  
    .  
    .  
 */  
```  
  
 The error occurs because the compiler recognizes the first `*/`, after the words `Open file`, as the end of the comment. It tries to process the remaining text and produces an error when it finds the `*/` outside a comment.  
  
 While you can use comments to render certain lines of code inactive for test purposes, the preprocessor directives `#if` and `#endif` and conditional compilation are a useful alternative for this task. For more information, see [Preprocessor Directives](../vs140/Preprocessor-Directives.md) in the *Preprocessor Reference*.  
  
 **Microsoft Specific**  
  
 The Microsoft compiler also supports single-line comments preceded by two forward slashes (**//**). If you compile with /Za (ANSI standard), these comments generate errors. These comments cannot extend to a second line.  
  
```  
// This is a valid comment  
```  
  
 Comments beginning with two forward slashes (**//**) are terminated by the next newline character that is not preceded by an escape character. In the next example, the newline character is preceded by a backslash (**\\**), creating an "escape sequence." This escape sequence causes the compiler to treat the next line as part of the previous line. (For more information, see [Escape Sequences](../vs140/Escape-Sequences.md).)  
  
```  
// my comment \  
    i++;   
```  
  
 Therefore, the `i++;` statement is commented out.  
  
 The default for Microsoft C is that the Microsoft extensions are enabled. Use /Za to disable these extensions.  
  
 **END Microsoft Specific**  
  
## See Also  
 [C Tokens](../vs140/C-Tokens.md)