---
title: "This array is fixed or temporarily locked (Visual Basic)"
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
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# This array is fixed or temporarily locked (Visual Basic)
This error has the following possible causes:  
  
-   Using `ReDim` to change the number of elements of a fixed-size array.  
  
-   Redimensioning a module-level dynamic array, in which one element has been passed as an argument to a procedure. If an element is passed, the array is locked to prevent deallocating memory for the reference parameter within the procedure.  
  
-   Attempting to assign a value to a `Variant` variable containing an array, but the `Variant` is currently locked.  
  
### To correct this error  
  
1.  Make the original array dynamic rather than fixed by declaring it with `ReDim` (if the array is declared within a procedure), or by declaring it without specifying the number of elements (if the array is declared at the module level.  
  
2.  Determine whether you really need to pass the element, since it is visible within all procedures in the module.  
  
3.  Determine what is locking the `Variant` and remedy it.  
  
## See Also  
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)