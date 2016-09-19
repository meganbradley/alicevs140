---
title: "CTypedPtrArray::GetAt"
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
ms.assetid: 16dfc974-1bed-4c73-beb3-b3ff235b4e57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrArray::GetAt
This inline function calls `BASE_CLASS`**::GetAt**.  
  
## Syntax  
  
```  
  
      TYPE GetAt(   
   INT_PTR nIndex    
) const;  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements stored in the array.  
  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `BASE_CLASS`**::GetUpperBound**.  
  
## Return Value  
 A copy of the element at the location specified by `nIndex`. This element is of the type specified by the template parameter *TYPE*.  
  
## Remarks  
 For more detailed remarks, see [CObArray::GetAt](../vs140/CObArray--GetAt.md)  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrArray Class](../vs140/CTypedPtrArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::GetAt](../vs140/CObArray--GetAt.md)   
 [CObArray::GetUpperBound](../vs140/CObArray--GetUpperBound.md)