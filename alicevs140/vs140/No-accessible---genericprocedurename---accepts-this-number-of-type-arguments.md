---
title: "No accessible &#39;&lt;genericprocedurename&gt;&#39; accepts this number of type arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ee942ba-0fa1-4ec1-9c2c-a0c0dc3f1b17
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# No accessible &#39;&lt;genericprocedurename&gt;&#39; accepts this number of type arguments
A statement calls a generic procedure that has more than one overloaded version, but none of the overloaded versions defines the same number of type parameters as the number of type arguments supplied in the call.  
  
 If there is only one generic version, you call it without type arguments, and the compiler can attempt *type inference*. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md). However, if there is more than one generic version, the compiler is not able to choose among them unless you supply type arguments. If you supply one type argument, you must supply a type argument for every type parameter that one of the overloaded versions defines.  
  
 **Error ID:** BC32118  
  
### To correct this error  
  
-   Decide which overloaded version you want to call, and then supply the appropriate number of type arguments.  
  
## See Also  
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)