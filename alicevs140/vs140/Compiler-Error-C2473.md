---
title: "Compiler Error C2473"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6bb7dbf5-b198-490f-860e-fd64d0c2a284
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2473
'identifier' : looks like a function definition, but there is no parameter list.  
  
 The compiler detected what looked like a function, without the parameter list.  
  
## Example  
 The following sample generates C2473.  
  
```  
// C2473.cpp  
// compile with: /clr /c  
class A {  
   int i {}   // C2473  
};  
  
class B {  
   int i() {}   // OK  
};  
```