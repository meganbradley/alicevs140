---
title: "Compiler Error C3069"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ca94291b-2bb4-4e3f-9acf-534234b83513
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3069
'operator': not allowed for enumeration type  
  
 An operator is not supported for CLR enumerations.  For more information, see [Using Operators and Enumerations](../vs140/Operators-and-Enumerations.md).  
  
## Example  
 The following sample generates C3069:  
  
```  
// C3069.cpp  
// compile with: /clr  
enum struct E { e1 };  
enum F { f1 };  
  
int main() {  
   E e = E::e1;  
   bool tf;  
   tf = !e;   // C3069  
  
   // supported for native enums  
   F f = f1;  
   tf = !f;  
}  
```