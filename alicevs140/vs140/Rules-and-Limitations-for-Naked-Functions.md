---
title: "Rules and Limitations for Naked Functions"
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
ms.topic: language-reference
ms.assetid: ff203858-2dd3-4a76-8a57-d0d06817adef
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Rules and Limitations for Naked Functions
## Microsoft Specific  
 The following rules and limitations apply to naked functions:  
  
-   The `return` statement is not permitted.  
  
-   Structured Exception Handling and C++ Exception Handling constructs are not permitted because they must unwind across the stack frame.  
  
-   For the same reason, any form of `setjmp` is prohibited.  
  
-   Use of the `_alloca` function is prohibited.  
  
-   To ensure that no initialization code for local variables appears before the prolog sequence, initialized local variables are not permitted at function scope. In particular, the declaration of C++ objects is not permitted at function scope. There may, however, be initialized data in a nested scope.  
  
-   Frame pointer optimization (the /Oy compiler option) is not recommended, but it is automatically suppressed for a naked function.  
  
-   You cannot declare C++ class objects at the function lexical scope. You can, however, declare objects in a nested block.  
  
-   The `naked` keyword is ignored when compiling with [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
-   For [__fastcall](../vs140/__fastcall.md) naked functions, whenever there is a reference in C/C++ code to one of the register arguments, the prolog code should store the values of that register into the stack location for that variable. For example:  
  
```  
// nkdfastcl.cpp  
// compile with: /c  
// processor: x86  
__declspec(naked) int __fastcall  power(int i, int j) {  
   // calculates i^j, assumes that j >= 0  
  
   // prolog  
   __asm {  
      push ebp  
      mov ebp, esp  
      sub esp, __LOCAL_SIZE  
     // store ECX and EDX into stack locations allocated for i and j  
     mov i, ecx  
     mov j, edx  
   }  
  
   {  
      int k = 1;   // return value  
      while (j-- > 0)   
         k *= i;  
      __asm {   
         mov eax, k   
      };  
   }  
  
   // epilog  
   __asm {  
      mov esp, ebp  
      pop ebp  
      ret  
   }  
}  
```  
  
## END Microsoft Specific  
  
## See Also  
 [Naked Function Calls](../vs140/Naked-Function-Calls.md)