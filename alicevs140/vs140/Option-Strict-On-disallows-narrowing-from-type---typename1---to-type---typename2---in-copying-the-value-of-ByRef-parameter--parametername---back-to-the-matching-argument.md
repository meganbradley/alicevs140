---
title: "Option Strict On disallows narrowing from type &#39;&lt;typename1&gt;&#39; to type &#39;&lt;typename2&gt;&#39; in copying the value of ByRef parameter &lt;parametername&gt;&#39; back to the matching argument"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc9ae5d2-b506-47cf-a50c-116fda5ed206
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On disallows narrowing from type &#39;&lt;typename1&gt;&#39; to type &#39;&lt;typename2&gt;&#39; in copying the value of ByRef parameter &lt;parametername&gt;&#39; back to the matching argument
A procedure call supplies a `ByRef` argument with a data type that widens to the argument's declared type, and `Option Strict` is `On`. The widening conversion is allowed when the argument is passed to the procedure, but when the procedure modifies the contents of the variable argument in the calling code, the reverse conversion is narrowing. Narrowing conversions are not allowed with `Option Strict On`.  
  
 **Error ID:** BC32029  
  
### To correct this error  
  
-   Supply each `ByRef` argument in the procedure call with the same data type as the declared type, or turn `Option Strict Off`.  
  
## See Also  
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Passing Arguments by Value and by Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)