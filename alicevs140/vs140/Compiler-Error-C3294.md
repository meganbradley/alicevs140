---
title: "Compiler Error C3294"
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
ms.assetid: 61b595e8-99bb-4740-88c3-96d66071ad6d
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3294
this syntax is not support with /clr:oldSyntax: please use 'function' instead  
  
 Features available in the new syntax for CLR programming are not available when compiling for Managed Extensions for C++.  
  
 For more information, see [Destructors and Finalizers](../vs140/Destructors-and-Finalizers-in-Visual-C--.md).  
  
## Example  
 The following sample generates C3294.  
  
```  
// C3294.cpp  
// compile with: /clr:oldSyntax /c  
__gc class R {  
protected:  
   !R() {}   // C3294  
   R() {}   // OK  
   ~R() {}   // OK  
};  
```