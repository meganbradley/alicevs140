---
title: "Compiler Error C2842"
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
ms.assetid: 8674f08d-9f50-46ad-9229-abc6b74fa0e5
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2842
'class' : a managed or WinRT type may not define its own 'operator new' or 'operator delete'  
  
 You can define your own [operator new](../vs140/operator-new---new--.md) or [operator delete](../vs140/operator-delete---new--.md) to manage memory allocation on the native heap. However, reference classes cannot define these operators because they are only allocated on the managed heap.  
  
 For more information, see [User-Defined Operators](../vs140/User-Defined-Operators--C---CLI-.md).  
  
## Example  
 The following sample generates C2842.  
  
```  
// C2842.cpp  
// compile with: /clr /c  
ref class G {  
   void* operator new( size_t nSize );   // C2842  
};  
```  
  
## Example  
 The following sample generates C2842.  
  
```  
// C2842_b.cpp  
// compile with: /clr:oldSyntax /c  
__gc class G {  
   void* operator new( size_t nSize );   // C2842  
};  
```