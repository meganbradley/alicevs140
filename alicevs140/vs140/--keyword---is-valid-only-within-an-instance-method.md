---
title: "&#39;&lt;keyword&gt;&#39; is valid only within an instance method"
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
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;keyword&gt;&#39; is valid only within an instance method
The `Me`, `MyClass`, and `MyBase` keywords refer to specific class instances. You cannot use them inside a shared `Function` or `Sub` procedure.  
  
 **Error ID:** BC30043  
  
### To correct this error  
  
-   Remove the keyword from the procedure, or remove the `Shared` keyword from the procedure declaration.  
  
## See Also  
 [Object Variable Assignment](../vs140/Object-Variable-Assignment--Visual-Basic-.md)   
 [Me, My, MyBase, and MyClass in Visual Basic](../vs140/Me--My--MyBase--and-MyClass-in-Visual-Basic.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)