---
title: "function (C-C++)"
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
H1: function (C/C++)
ms.assetid: cbd1bd60-fabf-4b5a-9c3d-2d9f4b871365
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# function (C-C++)
Specifies that calls to functions specified in the pragma's argument list be generated.  
  
## Syntax  
  
```  
  
#pragma function( function1 [, function2, ...] )  
```  
  
## Remarks  
 If you use the **intrinsic** pragma (or /Oi) to tell the compiler to generate intrinsic functions (intrinsic functions are generated as inline code, not as function calls), you can use the **function** pragma to explicitly force a function call. Once a function pragma is seen, it takes effect at the first function definition containing a specified intrinsic function. The effect continues to the end of the source file or to the appearance of an **intrinsic** pragma specifying the same intrinsic function. The **function** pragma can be used only outside of a function — at the global level.  
  
 For lists of the functions that have intrinsic forms, see [#pragma intrinsic](../vs140/intrinsic.md).  
  
## Example  
  
```  
// pragma_directive_function.cpp  
#include <ctype.h>  
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
  
// use intrinsic forms of memset and strlen  
#pragma intrinsic(memset, strlen)  
  
// Find first word break in string, and set remaining  
// chars in string to specified char value.  
char *set_str_after_word(char *string, char ch) {  
   int i;  
   int len = strlen(string);  /* NOTE: uses intrinsic for strlen */  
  
   for(i = 0; i < len; i++) {  
      if (isspace(*(string + i)))   
         break;  
   }  
  
   for(; i < len; i++)   
      *(string + i) = ch;  
  
   return string;  
}  
  
// do not use strlen intrinsic  
#pragma function(strlen)  
  
// Set all chars in string to specified char value.  
char *set_str(char *string, char ch) {  
   // Uses intrinsic for memset, but calls strlen library function  
   return (char *) memset(string, ch, strlen(string));  
}  
  
int main() {  
   char *str = (char *) malloc(20 * sizeof(char));  
  
   strcpy_s(str, sizeof("Now is the time"), "Now is the time");  
   printf("str is '%s'\n", set_str_after_word(str, '*'));  
   printf("str is '%s'\n", set_str(str, '!'));  
}  
```  
  
 **str is 'Now\*\*\*\*\*\*\*\*\*\*\*\*'**  
**str is '!!!!!!!!!!!!!!!'**   
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)