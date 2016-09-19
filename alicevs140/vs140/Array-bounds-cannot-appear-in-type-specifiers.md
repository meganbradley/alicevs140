---
title: "Array bounds cannot appear in type specifiers"
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
ms.assetid: 93b654f4-70fa-4a48-baed-ffae42075550
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array bounds cannot appear in type specifiers
Array sizes cannot be declared as part of a data type specifier.  
  
 **Error ID:** BC30638  
  
### To correct this error  
  
-   Specify the size of the array immediately following the variable name instead of placing the array size after the type, as shown in the following example.  
  
    ```  
    Dim Array(8) As Integer   
    ```  
  
-   Define an array and initialize it with the desired number of elements, as shown in the following example.  
  
    ```  
    Dim Array2() As Integer = New Integer(8) {}  
    ```  
  
## See Also  
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)