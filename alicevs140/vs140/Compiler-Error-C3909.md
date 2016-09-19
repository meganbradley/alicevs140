---
title: "Compiler Error C3909"
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
ms.assetid: 0a443132-e53f-42dc-a58b-f086da3e7bfd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3909
aWinRT or managed event declaration must occur in a WinRT or managed type  
  
 A Windows Runtime event or managed event was declared in a native type. To fix this error, declare events in Windows Runtime types or managed types.  
  
 For more information, see [event](../vs140/event---C---Component-Extensions-.md).  
  
 The following sample generates C3909 and shows how to fix it:  
  
```  
// C3909.cpp  
// compile with: /clr /c  
delegate void H();  
class X {  
   event H^ E;   // C3909 - use ref class X instead  
};  
  
ref class Y {  
   static event H^ E {  
      void add(H^) {}  
      void remove( H^ h ) {}  
      void raise( ) {}  
   }  
};  
```