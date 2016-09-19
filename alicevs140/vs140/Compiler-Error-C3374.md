---
title: "Compiler Error C3374"
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
ms.assetid: 41431299-bd20-47d4-a0c8-1334dd79018b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3374
can't take address of 'function' unless creating delegate instance  
  
 The address of a function was taken in a context other than the creation of a delegate instance.  
  
 The following sample generates C3374:  
  
```  
// C3374.cpp  
// compile with: /clr  
public delegate void MyDel(int i);  
  
ref class A {  
public:  
   void func1(int i) {  
      System::Console::WriteLine("in func1 {0}", i);  
   }  
};  
  
int main() {  
   &A::func1;   // C3374  
  
   // OK  
   A ^ a = gcnew A;  
   MyDel ^ StaticDelInst = gcnew MyDel(a, &A::func1);  
}  
```  
  
## See Also  
 [How to: Define and Use Delegates (C++/CLI)](../Topic/How%20to:%20Define%20and%20Use%20Delegates%20\(C++-CLI\).md)