---
title: "Methods or events that implement interface members cannot be declared &#39;Shared&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a24937c5-aeac-47de-a08b-d8696dd8221a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Methods or events that implement interface members cannot be declared &#39;Shared&#39;
You have attempted to declare as `Shared` a method or event that implements an interface member. Methods and events being implemented in a class cannot be designated `Shared` or `Private`, except in a non-inheritable class.  
  
 **Error ID:** BC30505  
  
### To correct this error  
  
-   Remove the `Shared` keyword.  
  
## See Also  
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)