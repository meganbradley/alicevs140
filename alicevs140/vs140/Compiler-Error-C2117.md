---
title: "Compiler Error C2117"
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
ms.assetid: b947379d-5861-42fc-ac26-170318579cbd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2117
'identifier' : array bounds overflow  
  
 An array has too many initializers:  
  
-   Array elements and initializers do not match in size and quantity.  
  
-   No space for the null terminator in a string.  
  
 The following sample generates C2117:  
  
```  
// C2117.cpp  
int main() {  
   char abc[4] = "abcd";   // C2117  
   char def[4] = "abd";   // OK  
}  
```