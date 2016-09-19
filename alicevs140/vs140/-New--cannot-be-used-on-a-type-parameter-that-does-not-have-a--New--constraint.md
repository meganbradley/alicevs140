---
title: "&#39;New&#39; cannot be used on a type parameter that does not have a &#39;New&#39; constraint"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7ec6b52d-6fd5-47a0-b4a2-163bfd3dae35
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;New&#39; cannot be used on a type parameter that does not have a &#39;New&#39; constraint
A declaration statement uses a [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md) clause specifying a type parameter as the type to be created, and the type parameter is declared without a `New` constraint.  
  
 A *constraint* on a type parameter imposes a requirement on any type argument passed to that type parameter when the generic type is created. The `New` constraint specifies that the type argument must expose a parameterless constructor that the creating code can access. This is what allows a `New` clause in a declaration statement to create an instance of that type.  
  
 **Error ID:** BC32046  
  
### To correct this error  
  
-   If you can require the type argument to expose an accessible parameterless constructor, add the `New` constraint to the declaration of the type parameter.  
  
-   If you cannot require the type argument to expose an accessible parameterless constructor, remove the `New` clause from the declaration statement. You cannot guarantee that any type argument passed to that type parameter permits creation of an instance.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)