---
title: "Compiler Error C2581"
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
ms.assetid: 24a4e4c1-24d3-4e42-b760-7dcaf9740b16
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2581
'type' : static 'operator =' function is illegal  
  
 The assignment (`=`) operator is incorrectly declared as `static`. Assignment operators cannot be `static`. For more information, see [User-Defined Operators](../vs140/User-Defined-Operators--C---CLI-.md).  
  
## Example  
 The following sample generates C2581.  
  
```  
// C2581.cpp  
// compile with: /clr /c  
ref struct Y {  
   static Y ^ operator = (Y^ me, int i);   // C2581  
   Y^ operator =(int i);   // OK  
};  
```