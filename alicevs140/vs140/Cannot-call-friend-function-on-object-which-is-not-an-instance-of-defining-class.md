---
title: "Cannot call friend function on object which is not an instance of defining class"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b9d821f0-8565-4f15-bb35-184789c69662
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cannot call friend function on object which is not an instance of defining class
Either you tried to call the `Friend` procedure of a class, or you tried to access a `Friend` property or method either cross-process or cross-thread. A `Friend` procedure is callable from a module outside the class, but is part of the project in which the class is defined.  
  
### To correct this error  
  
-   Ensure that you are calling or accessing the procedure from a module that is part of the project in which the class is defined.  
  
## See Also  
 [Friend](../Topic/Friend%20\(Visual%20Basic\).md)