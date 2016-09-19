---
title: "Local variables within generic methods cannot be declared &#39;Static&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cb5df484-76f9-4092-9d19-f26ddcf1c035
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Local variables within generic methods cannot be declared &#39;Static&#39;
The declaration of a local variable within a generic procedure specifies `Static`.  
  
 Visual Basic and the .NET Framework do not currently support any combination of static variables and generic procedures.  
  
 **Error ID:** BC32068  
  
### To correct this error  
  
-   Remove the `Static` keyword from the variable declaration.  
  
## See Also  
 [Static (Visual Basic)](../vs140/Static--Visual-Basic-.md)   
 [NOTINBUILD How to: Lengthen a Variable's Lifetime](assetId:///04e7c56c-1db0-4fe5-a678-859a39ec654b)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)