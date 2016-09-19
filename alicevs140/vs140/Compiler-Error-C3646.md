---
title: "Compiler Error C3646"
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
ms.assetid: 4391ead2-9637-4ca3-aeda-5a991b18d66d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3646
'specifier' : unknown override specifier  
  
 The compiler found a token in the position where it expected to find an override specifier, but the token was not recognized by the compiler.  
  
 For more information, see [Override Specifiers](../vs140/Override-Specifiers---C---Component-Extensions-.md).  
  
 The following sample generates C3646:  
  
```  
// C3646.cpp  
// compile with: /clr /c  
ref class C {  
   void f() unknown;   // C3646  
   // try the following line instead  
   // virtual void f() abstract;  
};  
```