---
title: "Multiple initializations of &#39;&lt;membername&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 574b6398-1e9d-43e1-ac16-6fc8687f71d9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Multiple initializations of &#39;&lt;membername&gt;&#39;
Multiple initializations of '<membername\>'. Fields and properties can be initialized only once in an object initializer expression.  
  
 You can assign an initial value to each field and property in an object initializer list only one time. The following declaration is not valid.  
  
```  
' Dim cust = New Customer() With {.Name = "Bob", .Name = "Robert"}  
```  
  
> [!NOTE]
>  You can use one field or property as the initial value for another member, as shown in the following declaration.  
  
```  
Dim cust = New Customer() With {.First = "Mike", .Last = "Nash", _  
                                .Full = .First & " " & .Last}  
```  
  
 **Error ID:** BC30989  
  
### To correct this error  
  
-   Eliminate all except one of the initializations for each field or property in the object initializer list.  
  
## See Also  
 [Object Initializers](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md)   
 [NOT IN BUILD: Property Procedures vs. Fields](assetId:///da1c05c1-87c7-40fa-b92c-e9c7e4d170f7)