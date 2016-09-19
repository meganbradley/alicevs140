---
title: "Overloading methods declared in multiple base interfaces is not valid"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7d1831c2-837c-4b02-8492-d0fc038fe184
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overloading methods declared in multiple base interfaces is not valid
Multiple inherited interfaces implicitly overload the same method.  
  
 **Error ID:** BC31410  
  
### To correct this error  
  
-   Use the `Shadows` modifier instead of the `Overloads` modifier.  
  
## See Also  
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Shadows](../vs140/Shadows--Visual-Basic-.md)