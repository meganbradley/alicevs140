---
title: "Argument matching parameter &#39;&lt;parametername&gt;&#39; narrows from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 652ff70b-156d-4d1c-af19-fa1c53e2d0b5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Argument matching parameter &#39;&lt;parametername&gt;&#39; narrows from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;
You have made a call to an overloaded method, but the compiler cannot find a method that can be called without a narrowing conversion. A narrowing conversion changes a value to a data type that might not be able to precisely hold some of the possible values.  
  
 **Error ID:** BC30520  
  
### To correct this error  
  
-   Specify `Option Strict Off`.  
  
## See Also  
 [Overloaded Properties and Methods](../vs140/Overloaded-Properties-and-Methods--Visual-Basic-.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)