---
title: "Compiler Error C3896"
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
ms.assetid: eb8be0f6-5b4e-4d71-8285-8a2a94f8ba29
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3896
'member' : improper initializer: this literal data member can only be initialized with 'nullptr'  
  
 A [literal](../vs140/literal--C---Component-Extensions-.md) data member was initialized incorrectly.  See [nullptr](../vs140/nullptr---C---Component-Extensions-.md) for more information.  
  
 The following sample generates C3896:  
  
```  
// C3896.cpp  
// compile with: /clr /c  
ref class R{};  
  
value class V {  
   literal R ^ r = "test";   // C3896  
   literal R ^ r2 = nullptr;   // OK  
};  
```