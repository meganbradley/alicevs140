---
title: "&#39;Declare&#39; statements are not allowed in generic types or types contained in generic types"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c620b67e-70f8-42ac-8292-e9ea484904c3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Declare&#39; statements are not allowed in generic types or types contained in generic types
A `Declare` statement appears as part of a generic class or structure, or a class or structure declared within a generic class or structure.  
  
 Visual Basic and the .NET Framework do not currently support any combination of external references and generic types. The compiler needs all the parameters and the return type of an external procedure to call it correctly.  
  
 **Error ID:** BC32075  
  
### To correct this error  
  
-   Move the `Declare` statement outside the scope of any generic type, or remove it altogether.  
  
## See Also  
 [Declare Statement](../Topic/Declare%20Statement.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)