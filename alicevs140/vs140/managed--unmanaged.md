---
title: "managed, unmanaged"
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
ms.assetid: f072ddcc-e1ec-408a-8ce1-326ddb60e4a4
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# managed, unmanaged
Enable function-level control for compiling functions as managed or unmanaged.  
  
## Syntax  
  
```  
  
      #pragma managed  
#pragma unmanaged  
#pragma managed([push,] on | off)  
#pragma managed(pop)  
```  
  
## Remarks  
 The [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) compiler option provides module-level control for compiling functions either as managed or unmanaged.  
  
 An unmanaged function will be compiled for the native platform, and execution of that portion of the program will be passed to the native platform by the common language runtime.  
  
 Functions are compiled as managed by default when **/clr** is used.  
  
 When applying these pragmas:  
  
-   Add the pragma preceding a function but not within a function body.  
  
-   Add the pragma after `#include` statements. Do not use these pragmas before `#include` statements.  
  
 The compiler ignores the `managed` and `unmanaged` pragmas if **/clr** is not used in the compilation.  
  
 When a template function is instantiated, the pragma state at the time of definition for the template determines if it is managed or unmanaged.  
  
 For more information, see [Initialization of Mixed Assemblies](../vs140/Initialization-of-Mixed-Assemblies.md).  
  
## Example  
  
```  
// pragma_directives_managed_unmanaged.cpp  
// compile with: /clr  
#include <stdio.h>  
  
// func1 is managed  
void func1() {  
   System::Console::WriteLine("In managed function.");  
}  
  
// #pragma unmanaged  
// push managed state on to stack and set unmanaged state  
#pragma managed(push, off)  
  
// func2 is unmanaged  
void func2() {  
   printf("In unmanaged function.\n");  
}  
  
// #pragma managed  
#pragma managed(pop)  
  
// main is managed  
int main() {  
   func1();  
   func2();  
}  
```  
  
 **In managed function.**  
**In unmanaged function.**   
## See Also  
 [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md)