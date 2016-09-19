---
title: "&#39;&lt;typename&gt;&#39; is a delegate type"
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
ms.assetid: dc6abba0-a9ad-450f-8899-87265bc84abc
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;typename&gt;&#39; is a delegate type
'<typename\>' is a delegate type. Delegate construction permits only a single AddressOf expression as an argument list. Often an AddressOf expression can be used instead of a delegate construction.  
  
 A `New` clause creating an instance of a delegate class supplies an invalid argument list to the delegate constructor.  
  
 You can supply only a single `AddressOf` expression when creating a new delegate instance.  
  
 This error can result if you do not pass any arguments to the delegate constructor, if you pass more than one argument, or if you pass a single argument that is not a valid `AddressOf` expression.  
  
 **Error ID:** BC32008  
  
### To correct this error  
  
-   Use a single `AddressOf` expression in the argument list for the delegate class in the `New` clause.  
  
## See Also  
 [New Operator](../vs140/New-Operator--Visual-Basic-.md)   
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [Delegates (Visual Basic)](../Topic/Delegates%20\(Visual%20Basic\).md)   
 [How to: Invoke a Delegate Method](../vs140/How-to--Invoke-a-Delegate-Method--Visual-Basic-.md)