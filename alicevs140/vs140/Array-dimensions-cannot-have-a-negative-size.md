---
title: "Array dimensions cannot have a negative size"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e310bd0d-f221-4b02-87f3-02124f4de87c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Array dimensions cannot have a negative size
One or more of the array bounds specified is a negative number. You can specify a negative subscript only when you use an upper bound of -1 to declare an empty array. Such an array has zero elements, but it is not `Nothing`.  
  
 **Error ID:** BC30611  
  
### To correct this error  
  
-   Replace the negative array bound with a positive number.  
  
## See Also  
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)