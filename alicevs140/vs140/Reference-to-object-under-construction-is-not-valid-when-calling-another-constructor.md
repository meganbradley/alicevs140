---
title: "Reference to object under construction is not valid when calling another constructor"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 68be49f1-e662-45c7-9998-e0006324535d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference to object under construction is not valid when calling another constructor
A reference was made to an object member before the object's constructor finished creating the object.  
  
 **Error ID:** BC31095  
  
### To correct this error  
  
-   Do not use `MyBase`, `MyClass`, or `Me` when calling a constructor from another constructor.  
  
## See Also  
 [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Using Constructors and Destructors](assetId:///548eebe1-86c4-4377-b2f5-447cb8be3d90)