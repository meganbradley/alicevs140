---
title: "Anonymous type must contain at least one member"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdc8dd47-ea38-49e8-8dd5-676f726cd101
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Anonymous type must contain at least one member
The initializer list in an anonymous type declaration cannot be empty.  
  
```  
' Not valid.  
' Dim anonInstance = New With {}  
```  
  
 **Error ID:** BC36574  
  
### To correct this error  
  
-   Declare a member within the braces, as shown in the following code.  
  
    ```  
    Dim anonInstance = New With {.MemberName = "value"}  
    ```  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)