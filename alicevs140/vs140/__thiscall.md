---
title: "__thiscall"
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
ms.assetid: a6a22dd2-0101-4885-b33b-22f6057965df
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __thiscall
## Microsoft Specific  
 The `__thiscall` calling convention is used on member functions and is the default calling convention used by C++ member functions that do not use variable arguments. Under `__thiscall`, the callee cleans the stack, which is impossible for `vararg` functions. Arguments are pushed on the stack from right to left, with the `this` pointer being passed via register ECX, and not on the stack, on the x86 architecture.  
  
 One reason to use `__thiscall` is in classes whose member functions use `__clrcall` by default. In that case, you can use `__thiscall` to make individual member functions callable from native code.  
  
 When compiling with [/clr:pure](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md), all functions and function pointers are `__clrcall` unless specified otherwise.  
  
 In releases before Visual C++ 2005, the thiscall calling convention could not be explicitly specified in a program, because `thiscall` was not a keyword.  
  
 `vararg` member functions use the `__cdecl` calling convention. All function arguments are pushed on the stack, with the `this` pointer placed on the stack last  
  
 Because this calling convention applies only to C++, there is no C name decoration scheme.  
  
 On ARM and [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)] machines, `__thiscall` is accepted and ignored by the compiler.  
  
 For non-static class functions, if the function is defined out-of-line, the calling convention modifier does not have to be specified on the out-of-line definition. That is, for class non-static member methods, the calling convention specified during declaration is assumed at the point of definition.  
  
## Example  
  
```  
// thiscall_cc.cpp  
// compile with: /c /clr:oldSyntax  
struct CMyClass {  
   void __thiscall mymethod();  
   void __clrcall mymethod2();  
};  
```  
  
## END Microsoft Specific  
  
## See Also  
 [Argument Passing and Naming Conventions](../vs140/Argument-Passing-and-Naming-Conventions.md)