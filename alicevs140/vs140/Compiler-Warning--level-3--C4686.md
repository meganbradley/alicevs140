---
title: "Compiler Warning (level 3) C4686"
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
ms.assetid: 767c83c2-9e4b-4f9e-88c8-02128ba563f4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4686
**'**   
 ***user-defined type* ' : possible change in behavior, change in UDT return calling convention**  
  
 A class template specialization was not is defined before it was used in a return type. Anything that instantiates the class will resolve C4686; declaring an instance or accessing a member (C<int\>::anything) are also options.  
  
 This warning is the result of work to make the Visual C++ .NET 2003 compiler conform to the ISO C++ standard.  
  
 This warning is off by default. See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.  
  
 Try the following instead,  
  
```  
// C4686.cpp  
// compile with: /W3  
#pragma warning (default : 4686)  
template <class T>  
class C;  
  
template <class T>  
C<T> f(T);  
  
template <class T>  
class C {};  
  
int main() {  
   f(1);   // C4686  
}  
  
template <class T>  
C<T> f(T) {  
   return C<int>();  
}  
```