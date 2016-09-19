---
title: "Option Strict On requires each lambda expression parameter to be declared with an &#39;As&#39; clause if its type cannot be inferred"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2aaa62b8-49c9-4ae8-b0f5-08e3f0b5ad10
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On requires each lambda expression parameter to be declared with an &#39;As&#39; clause if its type cannot be inferred
You have declared a parameter in a lambda expression without using an `As` clause, with `Option Strict` on.  
  
```  
' Not valid when Option Strict is on.  
' Dim increment1 = Function (n) n + 1  
```  
  
 The previous declaration is valid if the type of `n` can be inferred. For example, if you are assigning the previous lambda expression to a function delegate, `Del`:  
  
```  
Delegate Function Del(ByVal p As Integer) As Integer  
```  
  
 Now the type of `n` can be inferred from parameter `p`:  
  
```  
Dim increment2 as Del = Function(n) n + 1  
```  
  
 **Error ID:** BC36642  
  
### To correct this error  
  
-   Add an `As` clause to the parameter declaration:  
  
    ```  
    Dim increment3 = Function (n As Integer) n + 1  
    ```  
  
## See Also  
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)