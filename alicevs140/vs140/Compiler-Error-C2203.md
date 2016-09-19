---
title: "Compiler Error C2203"
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
ms.assetid: 5497df43-86f6-43d5-b6cb-723c4c589b10
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2203
delete operator cannot specify bounds for an array  
  
 With the **/Za** (ANSI) option, the `delete` operator can delete an entire array but not parts or specific members of the array.  
  
 The following sample generates C2203:  
  
```  
// C2203.cpp  
// compile with: /Za  
int main() {  
   int *ar = new int[10];  
   delete [4] ar;   // C2203  
   // try the following line instead  
   // delete [] ar;  
}  
```