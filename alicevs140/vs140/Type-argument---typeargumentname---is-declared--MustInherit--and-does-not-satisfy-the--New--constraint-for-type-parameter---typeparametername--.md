---
title: "Type argument &#39;&lt;typeargumentname&gt;&#39; is declared &#39;MustInherit&#39; and does not satisfy the &#39;New&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 597e5944-a61b-4858-ada5-efb80b27f26b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type argument &#39;&lt;typeargumentname&gt;&#39; is declared &#39;MustInherit&#39; and does not satisfy the &#39;New&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;
A generic type is invoked with a `MustInherit` class as a type argument, while the corresponding type parameter is declared with the `New` constraint.  
  
 The `New` constraint requires that the type passed in the corresponding type argument must support the creation of objects. However, an *abstract* class, that is, a class declared as `MustInherit`, does not expose any constructors because you cannot create any objects from it.  
  
 **Error ID:** BC32082  
  
### To correct this error  
  
1.  If the class used in the type argument does not need to be abstract, then remove the `MustInherit` keyword from its declaration.  
  
2.  If the class used in the type argument needs to be abstract but does not need to be used to construct the generic type, then pass a different class in the type argument.  
  
3.  If the corresponding type parameter does not need to create any objects from the type passed to it, then remove the `New` constraint from its declaration.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)