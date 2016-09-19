---
title: "String Literal Concatenation"
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
ms.assetid: 51486b1f-4b1e-4061-9add-1aa38c6cdb3c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# String Literal Concatenation
To form string literals that take up more than one line, you can concatenate the two strings. To do this, type a backslash, then press the RETURN key. The backslash causes the compiler to ignore the following newline character. For example, the string literal  
  
```  
"Long strings can be bro\  
ken into two or more pieces."  
```  
  
 is identical to the string  
  
```  
"Long strings can be broken into two or more pieces."  
```  
  
 String concatenation can be used anywhere you might previously have used a backslash followed by a newline character to enter strings longer than one line.  
  
 To force a new line within a string literal, enter the newline escape sequence (**\n**) at the point in the string where you want the line broken, as follows:  
  
```  
"Enter a number between 1 and 100\nOr press Return"  
```  
  
 Because strings can start in any column of the source code and long strings can be continued in any column of a succeeding line, you can position strings to enhance source-code readability. In either case, their on-screen representation when output is unaffected. For example:  
  
```  
printf_s ( "This is the first half of the string, "  
           "this is the second half ") ;  
```  
  
 As long as each part of the string is enclosed in double quotation marks, the parts are concatenated and output as a single string. This concatenation occurs according to the sequence of events during compilation specified by [translation phases](../vs140/Phases-of-Translation.md).  
  
```  
"This is the first half of the string, this is the second half"  
```  
  
 A string pointer, initialized as two distinct string literals separated only by white space, is stored as a single string (pointers are discussed in [Pointer Declarations](../vs140/Pointer-Declarations.md)). When properly referenced, as in the following example, the result is identical to the previous example:  
  
```  
char *string = "This is the first half of the string, "  
               "this is the second half";  
  
printf_s( "%s" , string ) ;  
```  
  
 In translation phase 6, the multibyte-character sequences specified by any sequence of adjacent string literals or adjacent wide-string literals are concatenated into a single multibyte-character sequence. Therefore, do not design programs to allow modification of string literals during execution. The ANSI C standard specifies that the result of modifying a string is undefined.  
  
## See Also  
 [C String Literals](../vs140/C-String-Literals.md)