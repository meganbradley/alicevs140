---
title: "Compiler Error C3072"
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
ms.assetid: cdd5cb6b-c478-4698-adfa-c40188d34a18
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3072
operator 'operator' cannot be applied to an instance of a ref class  
  
 use the unary '`operator` ' operator to convert an instance of a ref class to a handle type  
  
 A CLR type requires CLR operators, not native (or standard) operators.  For more information, see [% (Tracking Reference)](../vs140/Tracking-Reference-Operator--C---Component-Extensions-.md).  
  
## Example  
 The following sample generates C3072.  
  
```  
// C3072.cpp  
// compile with: /clr  
ref class R {};  
  
int main() {  
   R r1;  
   R^ r2 = &r1;   // C3072  
   R^ r3 = %r1;   // OK  
}  
```