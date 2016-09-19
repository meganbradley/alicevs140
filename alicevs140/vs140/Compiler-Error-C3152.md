---
title: "Compiler Error C3152"
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
ms.assetid: 4ee6e2cd-5d19-4b73-833d-765c35797e4b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3152
'construct' : 'keyword' can only be applied to a class, struct, or virtual member function  
  
 Certain keywords can only be applied to a C++ class.  
  
 The following sample generates C3152 and shows how to fix it:  
  
```  
// C3152.cpp  
// compile with: /clr /c  
ref class C {  
   int (*pfn)() sealed;   // C3152  
   virtual int g() sealed;   // OK  
};  
```  
  
 The following sample generates C3152 and shows how to fix it:  
  
```  
// C3152_2.cpp  
// compile with: /clr:oldSyntax /c  
__value __interface A {};   // C3152;  
__value class X {};   // OK  
```