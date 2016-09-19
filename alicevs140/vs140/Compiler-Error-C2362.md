---
title: "Compiler Error C2362"
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
ms.assetid: 7aafecbc-b3cf-45a6-9ec3-a17e3f222511
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2362
initialization of 'identifier' is skipped by 'goto label'  
  
 When compiling with [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md), jumping to the label prevents the identifier from being initialized.  
  
 You cannot jump past a declaration with an initializer unless the declaration is enclosed in a block that is not entered, or the variable has already been initialized.  
  
 The following sample generates C2326:  
  
```  
// C2362.cpp  
// compile with: /Za  
int main() {  
   goto label1;  
   int i = 1;      // C2362, initialization skipped  
label1:;  
}  
```  
  
 Possible resolution:  
  
```  
// C2362b.cpp  
// compile with: /Za  
int main() {  
   goto label1;  
   {  
      int j = 1;   // OK, this block is never entered  
   }  
label1:;  
}  
```