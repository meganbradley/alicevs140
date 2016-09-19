---
title: "How to: Use gcnew to Create Value Types and Use Implicit Boxing"
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
ms.assetid: ceb48841-d6bd-47be-a167-57f44c961603
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use gcnew to Create Value Types and Use Implicit Boxing
Using [gcnew](../vs140/ref-new--gcnew---C---Component-Extensions-.md) on a value type will create a boxed value type, which can then be placed on the managed, garbage-collected heap.  
  
## Example  
  
```  
// vcmcppv2_explicit_boxing4.cpp  
// compile with: /clr  
public value class V {  
public:  
   int m_i;  
   V(int i) : m_i(i) {}  
};  
  
public ref struct TC {  
   void do_test(V^ v) {  
      if (v != nullptr)  
         ;  
      else  
         ;  
   }  
};  
  
int main() {  
   V^ v = gcnew V(42);  
   TC^ tc = gcnew TC;  
   tc->do_test(v);  
}  
```  
  
## See Also  
 [Boxing](../vs140/Boxing---C---Component-Extensions-.md)