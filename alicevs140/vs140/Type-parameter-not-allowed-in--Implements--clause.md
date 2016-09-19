---
title: "Type parameter not allowed in &#39;Implements&#39; clause"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a62d773b-e878-4817-8638-da49849477d7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type parameter not allowed in &#39;Implements&#39; clause
An `Implements` clause in a generic type specifies a type parameter as the member to be implemented.  
  
 An `Implements` clause must specify an interface and a member. It can pass a type parameter to the interface, but it cannot pass it to the member, nor use it as the name of the member.  
  
 The following statements can generate this error.  
  
```  
Class c1(Of t)  
    Implements i1(Of t)  
    Public Sub doSomething() Implements t  
End Class  
```  
  
 **Error ID:** BC32056  
  
### To correct this error  
  
-   Specify the interface name and a genuine member of the interface following the `Implements` keyword. You can pass the type parameter to the interface if appropriate.  
  
    ```  
    Public Sub doSomething() Implements i1(Of t).doSomething  
    ```  
  
## See Also  
 [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md)   
 [NOT IN BUILD: Implements Keyword and Implements Statement](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)