---
title: "Compiler Error C3818"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: f9502f6a-0690-4135-ab88-cc97cf490f5c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3818
array property declaration 'property1' shall not overload an index property 'property2'  
  
 An overload is not possible for properties when one is an indexer and the other is an array property. See [__property](../vs140/__property.md) for more information.  
  
 C3818 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3818:  
  
```  
// C3818.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__gc class X {  
public:  
   __property int get_Int(int index) {  
      Console::WriteLine(S"Called indexed property");  
      return m_value;  
   }  
  
   __property int get_Int() __gc[] {   // C3818, rename a property  
      Console::WriteLine(S"Called array property");  
      return m_arr;  
   }  
  
   int m_arr __gc[];  
   int m_value;  
};  
  
int main() {  
   X* x = new X;  
   x->m_arr = new int __gc[3];  
   x->m_value = 3;  
  
   x->Int[0];  
}  
```