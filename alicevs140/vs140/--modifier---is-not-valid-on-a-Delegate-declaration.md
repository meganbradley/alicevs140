---
title: "&#39;&lt;modifier&gt;&#39; is not valid on a Delegate declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cacbcdc7-dca9-4a22-b3bf-7e264308c031
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;modifier&gt;&#39; is not valid on a Delegate declaration
You attempted to use a modifier, such as `Shared`, on a delegate declaration. Delegates are objects used to call the methods of other objects, by defining a constructor that is passed the specification of an object method. It is not valid to specify a modifier on a delegate declaration.  
  
 **Error ID:** BC30385  
  
### To correct this error  
  
1.  Remove the modifier.  
  
## See Also  
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [How to: Invoke a Delegate Method](../vs140/How-to--Invoke-a-Delegate-Method--Visual-Basic-.md)