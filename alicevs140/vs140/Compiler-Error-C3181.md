---
title: "Compiler Error C3181"
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
ms.assetid: 5d450f8b-6cef-4452-a0c4-2076e967451d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3181
'type' : invalid operand for operator  
  
 An invalid parameter was passed to the [__typeof](../vs140/__typeof.md) or [typeid](../Topic/typeid%20%20\(C++%20Component%20Extensions\).md) operator. The parameter must be a managed type.  
  
 Note that the compiler uses aliases for native types that map to types in the common language runtime.  
  
 The following sample generates C3181:  
  
```  
// C3181a.cpp  
// compile with: /clr  
using namespace System;  
  
int main() {  
   Type ^pType1 = interior_ptr<int>::typeid;   // C3181  
   Type ^pType2 = int::typeid;   // OK  
}  
```  
  
 The following sample generates C3181:  
  
```  
// C3181b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
int main() {  
   Type *pType1 = __typeof(int __gc*);   // C3181  
   Type *pType2 = __typeof(int*);   // OK  
}  
```