---
title: "Compiler Warning (level 3) C4390"
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
ms.assetid: c95c2f1b-9bce-4b1f-a80c-565d4cde0b1e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4390
';' : empty controlled statement found; is this the intent?  
  
 A semicolon was found after a control statement that contains no instructions.  
  
 If you get C4390 because of a macro, you should use the [warning](../vs140/warning.md) pragma to disable C4390 in the module containing the macro.  
  
 The following sample generates C4390:  
  
```  
// C4390.cpp  
// compile with: /W3  
int main() {  
   int i = 0;  
   if (i);   // C4390  
      i++;  
}  
```