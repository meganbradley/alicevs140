---
title: "Type constraint cannot be a &#39;NotInheritable&#39; class"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f45cc0b6-7df1-462a-b3df-c526c143e16a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type constraint cannot be a &#39;NotInheritable&#39; class
A constraint list includes a class that is marked as [NotInheritable](../vs140/NotInheritable--Visual-Basic-.md).  
  
 A constraint list on a type parameter can accept at most one class. A type argument supplied for that type parameter must inherit from that class. Therefore, the type parameter cannot accept a *sealed*, or `NotInheritable`, class as a constraint.  
  
 **Error ID:** BC32060  
  
### To correct this error  
  
-   If the type parameter must be able to inherit from the class, and you have control over the definition of the class, remove the `NotInheritable` declaration from the class.  
  
-   If the class must remain `NotInheritable`, you cannot use it as a constraint. Remove the class name from the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)