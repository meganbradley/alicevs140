---
title: "Object initializer syntax cannot be used to initialize an instance of type &#39;Object&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ef65965-f014-4fc1-8c7d-c603f0a764df
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Object initializer syntax cannot be used to initialize an instance of type &#39;Object&#39;
You cannot initialize an instance of `Object` by using object initializer syntax. An instance of `Object` has no properties or fields to assign a value to, and object initializer syntax requires at least one such property or field.  
  
```  
' Not valid.  
' Dim obj1 = New Object With {}  
' Dim obj2 = New Object With {.ToString = <some value>}  
```  
  
 **Error ID:** BC30994  
  
### To correct this error  
  
1.  Declare instances of type `Object` without using an initializer list:  
  
    ```  
    Dim obj3 as Object  
    Dim obj4 as New Object()  
    ```  
  
## See Also  
 [Object Initializers](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md)   
 [Object Data Type](../Topic/Object%20Data%20Type.md)