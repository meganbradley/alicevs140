---
title: "&#39;GoSub&#39; statements are no longer supported"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fef2d78f-39ba-4aad-93b3-c7a08df9f805
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;GoSub&#39; statements are no longer supported
`GoSub` cannot be used to call a procedure.  
  
 **Error ID:** BC30814  
  
### To correct this error  
  
-   Call procedures directly without using `GoSub`; for example:  
  
    ```  
    CalculateInterest(Amount, Rate, Time)  
    ```  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)