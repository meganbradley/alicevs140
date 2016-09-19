---
title: "Compiler Error C3084"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0362cb70-e24e-476f-a24d-8f5bb97c3afd
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3084
'function': a finalizer/destructor cannot be 'keyword'  
  
 A finalizer or destructor was declared incorrectly.  
  
 For example, a destructor should not be marked as sealed.  The destructor will be inaccessible to derived types.  For more information, see [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md) and [Destructors and Finalizers](../vs140/Destructors-and-Finalizers-in-Visual-C--.md).  
  
## Example  
 The following sample generates C3084.  
  
```  
// C3084.cpp  
// compile with: /clr /c  
ref struct R {  
protected:  
   !R() sealed;   // C3084  
   !R() abstract;   // C3084  
   !R();  
};  
```