---
title: "Compiler Error C2390"
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
ms.assetid: 06b749ee-d072-4db1-b229-715f2c0728b5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2390
'identifier' : incorrect storage class 'specifier'  
  
 The storage class is not valid for the global-scope identifier. The default storage class is used in place of the invalid class.  
  
 Possible resolutions:  
  
-   If the identifier is a function, declare it with `extern` storage.  
  
-   If the identifier is a formal parameter or local variable, declare it with auto storage.  
  
-   If the identifier is a global variable, declare it with no storage class (auto storage).  
  
## Example  
  
-   The following sample generates C2390:  
  
```  
// C2390.cpp  
register int i;   // C2390  
  
int main() {  
   register int j;   // OK  
}  
```