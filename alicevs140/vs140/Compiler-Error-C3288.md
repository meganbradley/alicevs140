---
title: "Compiler Error C3288"
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
ms.assetid: ed08a540-9751-46e1-9cbe-c51d6a49ffab
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3288
'type' : illegal dereference of a handle type  
  
 The compiler detected an illegal dereference of a handle type. You can dereference a handle type and assign it to a reference. For more information, see [% (Tracking Reference)](../vs140/Tracking-Reference-Operator--C---Component-Extensions-.md).  
  
## Example  
 The following sample generates C3288.  
  
```  
// C3288.cpp  
// compile with: /clr  
ref class R {};  
int main() {  
   *(System::Object^) nullptr;   // C3288  
  
// OK  
   (System::Object^) nullptr;   // OK  
   R^ r;  
   R% pr = *r;  
}  
```