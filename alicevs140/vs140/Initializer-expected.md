---
title: "Initializer expected"
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
ms.assetid: 6e183fe0-8888-43ed-a062-01571079455f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Initializer expected
You have tried to declare an instance of a class by using an object initializer in which the initialization list is empty, as shown in the following example.  
  
 `' Not valid.`  
  
 `' Dim aStudent As New Student With {}`  
  
 At least one field or property must be initialized in the initializer list, as shown in the following example.  
  
 `Dim aStudent As New Student With {.year = "Senior"}`  
  
 **Error ID:** BC30996  
  
### To correct this error  
  
1.  Initialize at least one field or property in the initializer, or do not use an object initializer.  
  
## See Also  
 [Object Initializers](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md)   
 [How to: Declare an Object by Using an Object Initializer](../vs140/How-to--Declare-an-Object-by-Using-an-Object-Initializer--Visual-Basic-.md)