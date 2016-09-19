---
title: "Compiler Error C2555"
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
ms.assetid: 5e49ebb8-7c90-457a-aa12-7ca7ab6574b2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2555
' class1::function1': overriding virtual function return type differs and is not covariant from 'class2::function2'  
  
 A virtual function and a derived overriding function have identical parameter lists but different return types. An overriding function in a derived class cannot differ from a virtual function in a base class only by its return type.  
  
 To resolve this error, cast the return value after the virtual function has been called.  
  
 You may also see this error if you compile with /clr.   For example, the Visual C++ equivalent to the following C# declaration:  
  
```  
Guid[] CheckSources(Guid sourceID, Guid[] carouselIDs);  
```  
  
 is  
  
```  
Guid CheckSources(Guid sourceID, Guid carouselIDs[]) [];  
```  
  
 For more information on C2555, see Knowledge Base article Q240862.  
  
 The following sample generates C2555:  
  
```  
// C2555.cpp  
// compile with: /c  
struct X {  
   virtual void func();  
};  
struct Y : X {  
   char func();  // C2555  
   void func2();   // OK  
};  
```