---
title: "Compiler Error C2562"
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
ms.assetid: 2c41e511-9952-4b98-9976-6b1523613e1b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2562
'identifier' : 'void' function returning a value  
  
 The function is declared as `void` but returns a value.  
  
 This error can be caused by an incorrect function prototype.  
  
 This error may be fixed if you specify the return type in the function declaration.  
  
 The following sample generates C2562:  
  
```  
// C2562.cpp  
// compile with: /c  
void testfunc() {  
   int i;  
   return i;   // C2562 delete the return to resolve  
}  
```