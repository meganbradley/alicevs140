---
title: "Instance members and &#39;Me&#39; cannot be used within a lambda expression in structures"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c24a7c7-50f6-4ffb-9ed2-07e2abc4eaf3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Instance members and &#39;Me&#39; cannot be used within a lambda expression in structures
From within a structure, you have defined a lambda expression that refers to an instance member of the structure or uses `Me`. The following code illustrates these two invalid references.  
  
```vb#  
Structure Structure1  
  
    Public InstanceMember As Integer  
  
    Public Function ExampleFun() As Integer  
        '' The error is caused by use of InstanceMember.  
        'Dim fun1 = Function() InstanceMember  
        '' The error is caused by use of Me.  
        'Dim fun2 = Function() Me.InstanceMember  
        'Return fun1()  
    End Function  
  
End Structure  
```  
  
 **Error ID:** BC36638  
  
### To correct this error  
  
-   Assign the instance member to a local variable, and use the local variable in your statement.  
  
    ```vb#  
    Public Function ExampleFunFix() As Integer  
        Dim temp = InstanceMember  
        Dim fun1 = Function() temp  
        Return fun1()  
    End Function  
    ```  
  
## See Also  
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)   
 [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2)   
 [Structure Statement](../Topic/Structure%20Statement.md)