---
title: "Constructor &#39;&lt;name&gt;&#39; cannot call itself"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d77b7f4-0640-4f89-9c65-f101fd2847c0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constructor &#39;&lt;name&gt;&#39; cannot call itself
A `Sub New` procedure in a class or structure calls itself.  
  
 The purpose of a constructor is to initialize an instance of a class or structure when it is first created. A class or structure can have several constructors, provided they all have different parameter lists. A constructor is permitted to call another constructor to perform its functionality in addition to its own. But it is meaningless for a constructor to call itself, and in fact it would result in infinite recursion if permitted.  
  
 **Error ID:** BC30298  
  
### To correct this error  
  
1.  Check the parameter list of the constructor being called. It should be different from that of the constructor making the call.  
  
2.  If you do not intend to call a different constructor, remove the `Sub New` call entirely.  
  
## See Also  
 [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)