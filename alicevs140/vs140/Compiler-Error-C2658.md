---
title: "Compiler Error C2658"
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
ms.assetid: 638368e8-7893-4a14-abec-13c768a9543a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2658
'member': redefinition in anonymous struct/union  
  
 Two anonymous structures or unions contained member declarations with the same identifier but with different types. Under [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md), you will also get this error for members with the same identifier and type.  
  
 The following sample generates C2658:  
  
```  
// C2658.cpp  
// compile with: /c  
struct X {  
   union { // can be struct too  
      int i;  
   };  
   union {  
      int i;   // Under /Za, C2658  
      // int i not needed here because it is defined in the first union  
   };  
};  
  
struct Z {  
   union {  
      char *i;  
   };  
  
   union {  
      void *i;   // C2658 redefinition of 'i'  
      // try the following line instead  
      // void *ii;  
   };  
};  
```