---
title: "&#39;ReDim&#39; statements require a parenthesized list of the new bounds of each dimension of the array"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2c5fea3-e7db-4797-b917-d61a65befbd4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;ReDim&#39; statements require a parenthesized list of the new bounds of each dimension of the array
You must specify the new size of an array as part of a `ReDim` statement.  
  
 **Error ID:** BC30670  
  
### To correct this error  
  
-   Supply the size of each rank of the array; for example:  
  
    ```  
    ReDim arr(5, 6)  
    ```  
  
## See Also  
 [ReDim Statement](../vs140/ReDim-Statement--Visual-Basic-.md)