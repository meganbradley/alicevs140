---
title: "Wrong number of type arguments passed to method &#39;&lt;genericprocedurename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 84c2f0cb-5706-4b4e-967c-0ca35a20913c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Wrong number of type arguments passed to method &#39;&lt;genericprocedurename&gt;&#39;
A generic procedure is called with a number of type arguments that does not match the number of type parameters with which it is defined.  
  
 **Error ID:** BC30951  
  
### To correct this error  
  
-   Supply a type argument for every type parameter defined for the generic procedure.  
  
     -or-  
  
-   Call the generic procedure with no type arguments at all, and let the compiler attempt to infer the type arguments.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)