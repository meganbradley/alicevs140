---
title: "&#39;&lt;method1&gt;&#39; and &#39;&lt;method2&gt;&#39; cannot overload each other because they differ only by the default values of optional parameters"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f07f925e-9f95-4885-bdba-eaba2d0483d8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;method1&gt;&#39; and &#39;&lt;method2&gt;&#39; cannot overload each other because they differ only by the default values of optional parameters
You have attempted to overload a method with another method that differs from the first only in its optional parameters. A method with an optional parameter is equivalent to two overloaded methods, one with the optional parameter, and the other without it. Therefore, you cannot overload a method with an argument list corresponding to either of these.  
  
 **Error ID:** BC30305  
  
### To correct this error  
  
-   Ensure that the methods are differentiated by more than only optional parameters.  
  
## See Also  
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md)