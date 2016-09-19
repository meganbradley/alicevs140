---
title: "Calling C Functions in Inline Assembly"
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
ms.assetid: f8a8d568-d175-4e23-9b24-36ef60a4cab3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Calling C Functions in Inline Assembly
## Microsoft Specific  
 An `__asm` block can call C functions, including C library routines. The following example calls the `printf` library routine:  
  
```  
// InlineAssembler_Calling_C_Functions_in_Inline_Assembly.cpp  
// processor: x86  
#include <stdio.h>  
  
char format[] = "%s %s\n";  
char hello[] = "Hello";  
char world[] = "world";  
int main( void )  
{  
   __asm  
   {  
      mov  eax, offset world  
      push eax  
      mov  eax, offset hello  
      push eax  
      mov  eax, offset format  
      push eax  
      call printf  
      //clean up the stack so that main can exit cleanly  
      //use the unused register ebx to do the cleanup  
      pop  ebx  
      pop  ebx  
      pop  ebx  
   }  
}  
```  
  
 Because function arguments are passed on the stack, you simply push the needed arguments — string pointers, in the previous example — before calling the function. The arguments are pushed in reverse order, so they come off the stack in the desired order. To emulate the C statement  
  
```  
printf( format, hello, world );  
```  
  
 the example pushes pointers to `world`, `hello`, and `format`, in that order, and then calls `printf`.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Inline Assembler](../vs140/Inline-Assembler.md)