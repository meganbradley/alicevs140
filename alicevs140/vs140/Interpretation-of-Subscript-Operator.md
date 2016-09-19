---
title: "Interpretation of Subscript Operator"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 8852ca18-9d5b-43f7-b8bd-abc89364fbf2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interpretation of Subscript Operator
Like other operators, the subscript operator (**[ ]**) can be redefined by the user. The default behavior of the subscript operator, if not overloaded, is to combine the array name and the subscript using the following method:  
  
 \*((*array-name*) + (*subscript*))  
  
 As in all addition that involves pointer types, scaling is performed automatically to adjust for the size of the type. Therefore, the resultant value is not *subscript* bytes from the origin of *array-name*; rather, it is the *subscript*th element of the array. (For more information about this conversion, see [Additive Operators](../vs140/Additive-Operators----and--.md).)  
  
 Similarly, for multidimensional arrays, the address is derived using the following method:  
  
 **((**   
 ***array-name* ) + (**   
 ***subscript* 1**  *max*2 *\* max*3*...max*n)               **+** *subscript*2 *\* max*3*...max*n)                    . . . *+* *subscript*n))  
  
## See Also  
 [Arrays](../vs140/Arrays--C---.md)