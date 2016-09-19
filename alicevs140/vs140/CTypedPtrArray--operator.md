---
title: "CTypedPtrArray::operator"
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
ms.topic: reference
ms.assetid: ef5231a0-e41d-4c29-93a1-b7c2b3bc1f36
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrArray::operator
These inline operators call `BASE_CLASS`**::operator [ ]**.  
  
## Syntax  
  
```  
  
      TYPE  
      & operator[ ](INT_PTR nIndex);  
TYPE operator[ ](INT_PTR nIndex) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements stored in the array.  
  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `BASE_CLASS`**::GetUpperBound**.  
  
## Remarks  
 The first operator, called for arrays that are not **const**, can be used on either the right (r-value) or the left (l-value) of an assignment statement. The second, invoked for **const** arrays, can be used only on the right.  
  
 The Debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrArray Class](../vs140/CTypedPtrArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::operator](../vs140/CObArray--operator.md)