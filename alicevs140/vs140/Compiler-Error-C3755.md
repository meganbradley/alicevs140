---
title: "Compiler Error C3755"
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
ms.assetid: 9317b55e-a52e-4b87-b915-5a208d6eda38
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3755
'delegate': a delegate may not be defined  
  
 A [delegate](../vs140/delegate---C---Component-Extensions-.md) can be declared but not defined.  
  
## Example  
 The following sample generates C3755.  
  
```  
// C3755.cpp  
// compile with: /clr /c  
delegate void MyDel() {};   // C3755  
```  
  
## Example  
 C3755 can also occur if you attempt to create a delegate template. The following sample generates C3755.  
  
```  
// C3755_b.cpp  
// compile with: /clr /c  
ref struct R {  
   template<class T>  
   delegate void D(int) {}   // C3755  
};  
```