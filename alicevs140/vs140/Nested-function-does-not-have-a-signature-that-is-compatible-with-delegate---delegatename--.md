---
title: "Nested function does not have a signature that is compatible with delegate &#39;&lt;delegatename&gt;&#39;"
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
ms.assetid: 493f292c-d81e-40ef-8b47-61f020571829
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Nested function does not have a signature that is compatible with delegate &#39;&lt;delegatename&gt;&#39;
A lambda expression has been assigned to a delegate that has an incompatible signature. For example, in the following code, delegate `Del` has two integer parameters.  
  
```vb#  
Delegate Function Del(ByVal p As Integer, ByVal q As Integer) As Integer  
```  
  
 The error is raised if a lambda expression with one argument is declared as type `Del`:  
  
```vb#  
' Neither of these is valid.   
' Dim lambda1 As Del = Function(n As Integer) n + 1  
' Dim lambda2 As Del = Function(n) n + 1  
```  
  
 **Error ID:** BC36532  
  
### To correct this error  
  
-   Adjust either the delegate definition or the assigned lambda expression so that the signatures are compatible.  
  
## See Also  
 [Relaxed Delegate Conversion](../vs140/Relaxed-Delegate-Conversion--Visual-Basic-.md)   
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)