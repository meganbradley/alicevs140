---
title: "initonly (C++-CLI)"
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
ms.topic: article
H1: initonly (C++/CLI)
ms.assetid: f745d7fa-dc08-46f1-9b97-0977be58a008
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# initonly (C++-CLI)
**initonly** is a context-sensitive keyword that indicates that variable assignment can occur only as part of the declaration or in a static constructor in the same class.  
  
 The following example shows how to use `initionly`:  
  
```  
// mcpp_initonly.cpp  
// compile with: /clr /c  
ref struct Y1 {  
   initonly  
   static int staticConst1;  
  
   initonly  
   static int staticConst2 = 0;  
  
   static Y1() {  
      staticConst1 = 0;  
   }  
};  
```  
  
## See Also  
 [Classes and Structs (Managed)](../vs140/Classes-and-Structs---C---Component-Extensions-.md)