---
title: "Compiler Error C3366"
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
ms.assetid: efc55bcf-c16d-43c1-a36f-87a6165fa2a8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3366
'variable' : static data members of managed or WinRTtypes must be defined within the class definition  
  
 You attempted to reference a static member of a WinRT or .NET class or interface outside the definition of that class or interface.  
  
 The compiler needs to know the full definition of the class (to emit the meta-data after one pass) and requires static data members to be initialized within the class.  
  
 For example, the following example generates C3366 and shows how to fix it:  
  
```  
// C3366.cpp  
// compile with: /clr /c  
ref class X {  
   public:  
   static int i;   // initialize i here to avoid C3366  
};  
  
int X::i = 5;      // C3366  
```  
  
 The following example generates C3366 and shows how to fix it:  
  
```  
// C3366_b.cpp  
// compile with: /clr:oldSyntax /c  
__gc struct X {  
   static int i;   // initialize i here to avoid C3366  
};  
  
int X::i = 5;      // C3366  
```