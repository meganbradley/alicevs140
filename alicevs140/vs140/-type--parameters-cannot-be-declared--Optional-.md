---
title: "&lt;type&gt; parameters cannot be declared &#39;Optional&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec4023e7-9ba6-4532-a6b9-4ae6b4f9063a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;type&gt; parameters cannot be declared &#39;Optional&#39;
A definition of a delegate, event, or operator declares an [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) parameter.  
  
 `Optional` parameters are allowed only on `Declare`, `Function`, `Property`, and `Sub` parameters.  
  
 **Error ID:** BC33010  
  
### To correct this error  
  
-   Remove the `Optional` keyword from the parameter list.  
  
-   If you are defining an operator, you might be able to achieve the `Optional` functionality with a series of overloads.  
  
-   If you are defining a delegate or event, you must rework the overall logic of this part of your application. You cannot use `Optional` or [ParamArray](../vs140/ParamArray--Visual-Basic-.md) parameters, or overloaded versions, on delegate or event parameters.  
  
## See Also  
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)