---
title: "Number of indices exceeds the number of dimensions of the indexed array"
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
ms.assetid: 2c5363e1-62c2-4f5a-b675-c7337aeb363d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Number of indices exceeds the number of dimensions of the indexed array
The number of indices used to access an array element must be exactly the same as the rank of the array, that is, the number of dimensions declared for it.  
  
 **Error ID:** BC30106  
  
### To correct this error  
  
-   Remove subscripts from the array reference until the total number of subscripts equals the rank of the array. For example:  
  
    ```  
    [Visual Basic]  
    Dim gameBoard(3, 3) As String  
  
    ' Incorrect code. The array has two dimensions.  
    gameBoard(1, 1, 1) = "X"  
    gameBoard(2, 1, 1) = "O"  
  
    ' Correct code.  
    gameBoard(0, 0) = "X"  
    gameBoard(1, 0) = "O"  
    ```  
  
## See Also  
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)