---
title: "How to: Overload Functions with Interior Pointers and Native Pointers (C++-CLI)"
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
H1: How to: Overload Functions with Interior Pointers and Native Pointers (C++/CLI)
ms.assetid: d70df625-4aad-457c-84f5-70a0a290cc1f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Overload Functions with Interior Pointers and Native Pointers (C++-CLI)
Functions can be overloaded depending on whether the parameter type is an interior pointer or a native pointer.  
  
> [!IMPORTANT]
>  This language feature is supported by the **/clr** compiler option, but not by the **/ZW** compiler option.  
  
## Example  
  
### Code  
  
```  
// interior_ptr_overload.cpp  
// compile with: /clr  
using namespace System;  
  
// C++ class  
struct S {  
   int i;  
};  
  
// managed class  
ref struct G {  
   int i;  
};  
  
// can update unmanaged storage  
void f( int* pi ) {  
   *pi = 10;  
   Console::WriteLine("in f( int* pi )");  
}  
  
// can update managed storage  
void f( interior_ptr<int> pi ) {  
   *pi = 10;   
   Console::WriteLine("in f( interior_ptr<int> pi )");  
}  
  
int main() {  
   S *pS = new S;   // C++ heap  
   G ^pG = gcnew G;   // common language runtime heap  
   f( &pS->i );  
   f( &pG->i );  
};  
```  
  
### Output  
  
```  
in f( int* pi )  
in f( interior_ptr<int> pi )  
```  
  
## See Also  
 [interior_ptr (C++/CLI)](../vs140/interior_ptr--C---CLI-.md)