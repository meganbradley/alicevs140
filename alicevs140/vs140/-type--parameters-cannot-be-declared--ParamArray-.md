---
title: "&lt;type&gt; parameters cannot be declared &#39;ParamArray&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: faba9aef-ca4e-4c4d-934c-a3e3d3fa3c3e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;type&gt; parameters cannot be declared &#39;ParamArray&#39;
A definition of a delegate, event, or operator declares a [ParamArray](../vs140/ParamArray--Visual-Basic-.md) parameter.  
  
 `ParamArray` parameters are allowed only on `Declare`, `Function`, `Property`, and `Sub` parameters.  
  
 **Error ID:** BC33009  
  
### To correct this error  
  
-   Remove the `ParamArray` keyword from the parameter list.  
  
-   If you are defining an operator, you might be able to achieve the `ParamArray` functionality with a series of overloads.  
  
-   If you are defining a delegate or event, you must rework the overall logic of this part of your application. You cannot use [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) or `ParamArray` parameters, or overloaded versions, on delegate or event parameters.  
  
## See Also  
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)