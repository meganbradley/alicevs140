---
title: "Either the parameter type or the return type of this conversion operator must be the containing type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55baff11-eb35-4c81-bc04-5006524ab450
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Either the parameter type or the return type of this conversion operator must be the containing type
A definition of a conversion operator specifies both the parameter and the return type with types other than that of the class or structure in which the operator is defined.  
  
 When you define a conversion operator in a class or structure, it must convert to or from the type of that class or structure.  
  
 **Error ID:** BC33022  
  
### To correct this error  
  
-   Change the parameter type or the return type to the type of the class or structure in which the operator is defined.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)