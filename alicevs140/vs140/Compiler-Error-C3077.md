---
title: "Compiler Error C3077"
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
ms.assetid: d9f3c619-d1e2-4656-81a5-a35a9586a7d4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3077
'finalizer' : a finalizer can only be a member of a reference type  
  
 You cannot declare a finalizer in a native or value type.  
  
 For more information, see [Destructors and Finalizers](../vs140/Destructors-and-Finalizers-in-Visual-C--.md).  
  
## Example  
 The following sample generates C3077.  
  
```  
// C3077.cpp  
// compile with: /clr /c  
value struct vs {  
   !vs(){}   // C3077  
};  
  
ref struct rs {  
protected:  
   !rs(){}   // OK  
};  
```