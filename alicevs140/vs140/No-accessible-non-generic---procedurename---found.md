---
title: "No accessible non-generic &#39;&lt;procedurename&gt;&#39; found"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7bf8b67-8a0a-499e-9992-dc00e09b7ff4
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# No accessible non-generic &#39;&lt;procedurename&gt;&#39; found
A statement calls a procedure that has more than one overloaded version, but all the overloaded versions are generic and the call does not supply type arguments.  
  
 If there is only one generic version and you call it without type arguments, the compiler can attempt *type inference*. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md). However, if there is more than one generic version, the compiler is not able to choose among them unless you supply type arguments. If you supply one type argument, you must supply a type argument for every type parameter that one of the overloaded versions defines.  
  
 **Error ID:** BC32117  
  
### To correct this error  
  
-   Call the procedure with a type argument list.  
  
## See Also  
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)