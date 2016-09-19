---
title: "Exception Specifications (throw) (C++)"
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
ms.assetid: 4d3276df-6f31-4c7f-8cab-b9d2d003a629
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exception Specifications (throw) (C++)
Exception specifications are a C++ language feature that is deprecated in C++11. They were designed to provide summary information about what exceptions can be thrown out of a function, but in practice they were found to be problematic. The one exception specification that did prove to be somewhat useful was the throw() specification. For example:  
  
```  
void MyFunction(int i) throw();  
```  
  
 tells the compiler that the function does not throw any exceptions. It is the equivalent to using [__declspec(nothrow)](../vs140/nothrow--C---.md). Its use is considered optional.  
  
 **(C++11)** In the ISO C++11 Standard, [noexcept](../vs140/noexcept--C---.md) operator was introduced and is supported in Visual Studio 2015 and later. Whenever possible, use `noexcept` to specify whether a function might throw exceptions.  
  
 Visual C++ departs from the ISO C++ Standard in its implementation of exception specifications.  The following table summarizes the Visual C++ implementation of exception specifications:  
  
|Exception specification|Meaning|  
|-----------------------------|-------------|  
|throw()|The function does not throw an exception. However, if an exception is thrown out of a function marked throw(), the Visual C++ compiler will not call unexpected (see [unexpected (CRT)](../vs140/unexpected--CRT-.md) and [unexpected (<exception\>)](../vs140/unexpected---exception--.md) for more information). If a function is marked with throw(), the Visual C++ compiler will assume that the function does not throw C++ exceptions and generate code accordingly. Due to code optimizations that might be performed by the C++ compiler (based on the assumption that the function does not throw any C++ exceptions) if a function does throw an exception, the program may not execute correctly.|  
|throw(...)|The function can throw an exception.|  
|throw(`type`)|The function can throw an exception of type `type`. However, in Visual C++ .NET, this is interpreted as throw(...).  See [Function Exception Specifiers](../vs140/15.4-Function-Exception-Specifiers.md).|  
  
 If exception handling is used in an application, there must be one or more functions that handle thrown exceptions. Any functions called between the one that throws an exception and the one that handles the exception must be capable of throwing the exception.  
  
 The throw behavior of a function depends on the following factors:  
  
-   Whether you are compiling the function under C or C++.  
  
-   Which [/EH](../vs140/-EH--Exception-Handling-Model-.md) compiler option you use.  
  
-   Whether you explicitly specify the exception specification.  
  
 Explicit exception specifications are not allowed on C functions.  
  
 The following table summarizes the throw behavior of a function:  
  
|Function|/EHsc|/EHs|/EHa|/EHac|  
|--------------|------------|-----------|-----------|------------|  
|C function|throw()|throw(...)|throw(...)|throw(...)|  
|C++ function with no exception specification|throw(...)|throw(...)|throw(...)|throw(...)|  
|C++ function with throw() exception specification|throw()|throw()|throw(...)|throw(...)|  
|C++ function with throw(...) exception specification|throw(...)|throw(...)|throw(...)|throw(...)|  
|C++ function with throw(`type`) exception specification|throw(...)|throw(...)|throw(...)|throw(...)|  
  
## Example  
  
```cpp  
// exception_specification.cpp  
// compile with: /EHs  
#include <stdio.h>  
  
void handler() {  
   printf_s("in handler\n");  
}  
  
void f1(void) throw(int) {  
   printf_s("About to throw 1\n");  
   if (1)  
      throw 1;  
}  
  
void f5(void) throw() {  
   try {  
      f1();  
   }  
   catch(...) {  
      handler();  
    }  
}  
  
// invalid, doesn't handle the int exception thrown from f1()  
// void f3(void) throw() {  
//   f1();  
// }  
  
void __declspec(nothrow) f2(void) {  
   try {  
      f1();  
   }  
   catch(int) {  
      handler();  
    }  
}  
  
// only valid if compiled without /EHc   
// /EHc means assume extern "C" functions don't throw exceptions  
extern "C" void f4(void);  
void f4(void) {  
   f1();  
}  
  
int main() {  
   f2();  
  
   try {  
      f4();  
   }  
   catch(...) {  
      printf_s("Caught exception from f4\n");  
   }  
   f5();  
}  
```  
  
 **About to throw 1**  
**in handler**  
**About to throw 1**  
**Caught exception from f4**  
**About to throw 1**  
**in handler**   
## See Also  
 [try, throw, and catch Statements (C++)](../vs140/try--throw--and-catch-Statements--C---.md)   
 [C++ Exception Handling](../vs140/C---Exception-Handling.md)