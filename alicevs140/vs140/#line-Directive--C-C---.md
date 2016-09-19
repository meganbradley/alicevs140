---
title: "#line Directive (C-C++)"
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
H1: #line Directive (C/C++)
ms.assetid: 585c1dc4-5184-4f01-98f4-80c1909744d7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #line Directive (C-C++)
The `#line` directive tells the preprocessor to change the compiler's internally stored line number and filename to a given line number and filename.  
  
## Syntax  
  
```  
  
#line   
digit-sequence ["filename"]  
```  
  
## Remarks  
 The compiler uses the line number and optional filename to refer to errors that it finds during compilation. The line number usually refers to the current input line, and the filename refers to the current input file. The line number is incremented after each line is processed.  
  
 The *digit-sequence* value can be any integer constant. Macro replacement can be performed on the preprocessing tokens, but the result must evaluate to the correct syntax. The *filename* can be any combination of characters and must be enclosed in double quotation marks (**" "**). If *filename* is omitted, the previous filename remains unchanged.  
  
 You can alter the source line number and filename by writing a `#line` directive. The translator uses the line number and filename to determine the values of the predefined macros **__FILE\_\_** and **__LINE\_\_**. You can use these macros to insert self-descriptive error messages into the program text. For more information on these predefined macros, see [Predefined Macros](../vs140/Predefined-Macros.md).  
  
 The **__FILE\_\_** macro expands to a string whose contents are the filename, surrounded by double quotation marks (**" "**).  
  
 If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values. The `#line` directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.  
  
 The following examples illustrate `#line` and the **__LINE\_\_** and **__FILE\_\_** macros.  
  
 In this statement, the internally stored line number is set to 151 and the filename is changed to `copy.c`.  
  
```  
#line 151 "copy.c"  
```  
  
 In this example, the macro `ASSERT` uses the predefined macros **__LINE\_\_** and **__FILE\_\_** to print an error message about the source file if a given "assertion" is not true.  
  
```  
#define ASSERT(cond)  
  
if( !(cond) )\  
{printf( "assertion error line %d, file(%s)\n", \  
__LINE__, __FILE__ );}  
```  
  
## See Also  
 [Preprocessor Directives](../vs140/Preprocessor-Directives.md)