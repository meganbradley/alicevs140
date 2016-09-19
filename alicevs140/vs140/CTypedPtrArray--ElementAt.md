---
title: "CTypedPtrArray::ElementAt"
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
ms.assetid: 9f3c8b16-86e0-4c4e-8409-dd985c8a287a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrArray::ElementAt
This inline function calls `BASE_CLASS`**::ElementAt**.  
  
## Syntax  
  
```  
  
      TYPE& ElementAt(   
   INT_PTR nIndex    
);  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of elements stored in this array.  
  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `BASE_CLASS`**::GetUpperBound**.  
  
## Return Value  
 A temporary reference to the element at the location specified by `nIndex`. This element is of the type specified by the template parameter *TYPE*.  
  
## Remarks  
 For more detailed remarks, see [CObArray::ElementAt](../vs140/CObArray--ElementAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrArray Class](../vs140/CTypedPtrArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::ElementAt](../vs140/CObArray--ElementAt.md)   
 [CObArray::GetUpperBound](../vs140/CObArray--GetUpperBound.md)