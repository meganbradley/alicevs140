---
title: "Events of shared WithEvents variables cannot be handled by non-shared methods"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5b9fceb4-ab11-41bb-ad3b-6f1a9da8ae7e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Events of shared WithEvents variables cannot be handled by non-shared methods
A variable declared with the `Shared` modifier is a shared variable. A shared variable identifies exactly one storage location. A variable declared with the `WithEvents` modifier asserts that the type to which the variable belongs handles the set of events the variable raises. When a value is assigned to the variable, the property created by the `WithEvents` declaration unhooks any existing event handler and hooks up the new event handler via the `Add` method.  
  
 **Error ID:** BC30594  
  
### To correct this error  
  
-   Declare your event handler `Shared`.  
  
## See Also  
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)   
 [WithEvents](../vs140/WithEvents--Visual-Basic-.md)