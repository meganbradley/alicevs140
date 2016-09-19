---
title: "Explicit initialization is not permitted with multiple variables declared with a single type specifier"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57bbdd58-b58d-4144-8fa6-366a7167df27
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Explicit initialization is not permitted with multiple variables declared with a single type specifier
Initialization is not allowed when multiple variables are declared on the same line.  
  
 **Error ID:** BC30671  
  
### To correct this error  
  
1.  Declare and initialize each item separately.  
  
2.  Declare multiple items together and then initialize each item; for example:  
  
    ```  
    Dim x, b, i As Integer  
    x = 9 : b = 9 : i = 9   
    ' ":" is the same as a new line.  
    ```  
  
## See Also  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Variable Declaration](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)