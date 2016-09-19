---
title: "Constraint type &#39;&lt;typename&gt;&#39; already specified for this type parameter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b0e85e9-3ac8-4181-97de-ca690b95a63c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constraint type &#39;&lt;typename&gt;&#39; already specified for this type parameter
A constraint list includes a class or interface constraint more than once.  
  
 A constraint list imposes requirements on the type argument passed to the type parameter. You can specify the following requirements in any combination:  
  
-   The type argument must implement one or more interfaces  
  
-   The type argument must inherit from at most one class  
  
 A type cannot implement or inherit from the same type more than once, and you cannot specify a type more than once in the same constraint list.  
  
 **Error ID:** BC32071  
  
### To correct this error  
  
-   Remove any redundant specifications of the same class or interface. It should appear only once in the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)