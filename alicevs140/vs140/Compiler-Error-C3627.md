---
title: "Compiler Error C3627"
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
ms.assetid: 905ad0a0-8c49-4187-b66e-b375f5a1fae5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3627
Only a value type can be boxed  
  
 Only value classes can be boxed.  
  
 The following sample generates C3627:  
  
```  
// C3627.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__value class vA {  
};  
  
__gc class A {  
};  
  
int main()  
{  
   A* a;  
   __box(a);   // C3627  
  
   // box a value type  
   vA va;  
   __box(va);  
}  
```