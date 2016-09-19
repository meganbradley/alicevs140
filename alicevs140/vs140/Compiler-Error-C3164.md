---
title: "Compiler Error C3164"
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
ms.assetid: c5ed7323-136b-44f1-9794-aaa36daa706a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3164
'member': Copy constructors and destructors on value types are not supported  
  
 Copy constructors and destructors are not supported on [__value](../vs140/__value.md) types.  
  
 C3164 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3164:  
  
```  
// C3164.cpp  
// compile with: /clr:oldSyntax /c  
__value class MyClass {  
public:  
   ~MyClass();   // C3164  
   MyClass(const MyClass& f);   // C3164  
};  
```