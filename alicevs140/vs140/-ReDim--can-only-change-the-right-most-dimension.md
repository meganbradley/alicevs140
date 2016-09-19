---
title: "&#39;ReDim&#39; can only change the right-most dimension"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;ReDim&#39; can only change the right-most dimension
A `ReDim` statement attempted to use the `Preserve` keyword to change a dimension of an array that is not the last dimension. When using `Preserve`, you can resize only the last dimension of an array. For all other dimensions, you must specify the same size as for the existing array.  
  
### To correct this error  
  
-   Remove the `Preserve` keyword.  
  
## See Also  
 [NOTINBUILD Overview of Arrays in Visual Basic](assetId:///ca50e2f2-b4d2-4c57-9169-9abbcc3392d8)   
 [NOTINBUILD Multidimensional Arrays in Visual Basic](assetId:///d92cad25-07e2-4d79-8ea4-ab269700f5de)   
 [ReDim Statement](../vs140/ReDim-Statement--Visual-Basic-.md)   
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Preserve - delete](assetId:///91badeab-b4e0-48b6-92c9-9f0c8f995d81)