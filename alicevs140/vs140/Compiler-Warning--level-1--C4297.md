---
title: "Compiler Warning (level 1) C4297"
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
ms.topic: error-reference
ms.assetid: ba92fcdc-9f70-4f60-abe6-281f9582ca59
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4297
'function' : function assumed not to throw an exception but does  
  
 A function declaration contains a (possibly implicit) `noexcept` specifier, an empty `throw` exception specifier, or a [__declspec(nothrow)](../vs140/nothrow--C---.md) attribute, and the definition contains one or more [throw](../vs140/try--throw--and-catch-Statements--C---.md) statements. To resolve C4297, do not attempt to throw exceptions in functions that are declared `__declspec(nothrow)`, `noexcept(true)` or `throw()`. Alternatively, remove the `noexcept`, `throw()`, or `__declspec(nothrow)` specification.  
  
 By default, the compiler generates implicit `noexcept(true)` specifiers for user-defined destructors and deallocator functions and compiler-generated special member functions. This conforms to the ISO C++11 standard. To prevent generation of implicit noexcept specifiers and revert the compiler to the non-standard behavior of Visual Studio 2013, use the **/Zc:implicitNoexcept-** compiler option. For more information, see [/Zc:implicitNoexcept](../vs140/-Zc-implicitNoexcept--Implicit-Exception-Specifiers-.md).  
  
 For more information on exception specifications, see [Exception Specifications](../vs140/Exception-Specifications--throw---C---.md). Also, see [/EH](../vs140/-EH--Exception-Handling-Model-.md) for information on how to modify exception handling behavior at compile time.  
  
 This warning is also generated for __declspec([dllexport](../vs140/dllexport--dllimport.md)) functions marked extern "C", even if they are C++ functions.  
  
 The following sample generates C4297:  
  
```  
// C4297.cpp  
// compile with: /W1 /LD  
void __declspec(nothrow) f1()   // declared nothrow  
// try the following line instead  
// void f1()  
{  
   throw 1;   // C4297  
}  
```