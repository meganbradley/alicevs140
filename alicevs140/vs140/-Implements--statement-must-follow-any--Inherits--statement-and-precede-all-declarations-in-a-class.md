---
title: "&#39;Implements&#39; statement must follow any &#39;Inherits&#39; statement and precede all declarations in a class"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8036a1a1-7e31-4c49-b74b-01601a548f3e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Implements&#39; statement must follow any &#39;Inherits&#39; statement and precede all declarations in a class
An `Implements` statement was encountered in an invalid location.  
  
 **Error ID:** BC31053  
  
### To correct this error  
  
-   Place `Implements` statements immediately following any `Inherits` statements, but before any declarations. For example:  
  
    ```  
    Class Derived  
       Inherits Base  
       Implements One  
       Sub SubOne() Implements One.Method1  
          ' Add code to implement the method.  
       End Sub  
    End Class  
    ```  
  
## See Also  
 [Interfaces](../vs140/Interfaces--Visual-Basic-.md)   
 [Implements](../vs140/Implements-Clause--Visual-Basic-.md)