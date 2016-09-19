---
title: "Compiler Error C2814"
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
ms.assetid: 7d165136-a08b-4497-a76d-60a21bb19404
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2814
'member' : a native type cannot be nested within a managed or WinRT type 'type'  
  
## Example  
 A native type cannot be nested in a CLR or WinRT type. The following sample generates C2814 and shows how to fix it.  
  
```  
// C2814.cpp  
// compile with: /clr /c  
ref class A {  
   class B {};   // C2814  
   ref class C {};   // OK  
};  
```  
  
## Example  
 Using Managed Extensions for C++, you must explicitly specify the "managed-ness" of an embedded type using one of the following keywords: [__gc](../vs140/__gc.md), [__nogc](../vs140/__nogc.md), or [__value](../vs140/__value.md).  
  
 The following sample generates C2814 and shows how to fix it.  
  
```  
// C2814_b.cpp  
// compile with: /clr:oldSyntax /c  
__gc class A {  
   class B {};   // C2814  
   __gc class C {};   // OK  
};  
```