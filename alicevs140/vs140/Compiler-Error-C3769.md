---
title: "Compiler Error C3769"
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
ms.assetid: 341675e1-7428-4da6-8275-1b2f0a70dacc
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3769
'type' : a nested class cannot have the same name as the immediately enclosing class  
  
 A nested class cannot have the same name as the immediately enclosing class.  
  
## Example  
 The following sample generates C3769.  
  
```  
// C3769.cpp  
// compile with: /c  
class x {  
   class x {};   // C3769  
   class y {  
      class x{};   // OK  
   };  
};  
```