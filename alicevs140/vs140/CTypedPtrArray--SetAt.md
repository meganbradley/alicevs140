---
title: "CTypedPtrArray::SetAt"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: b8f7ca70-c8e3-4a76-8f1e-9dc003ded110
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrArray::SetAt
This member function calls `BASE_CLASS`**::SetAt**.  
  
## Syntax  
  
```  
  
      void SetAt(   
   INT_PTR nIndex,   
   TYPE ptr    
);  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by [CObArray::GetUpperBound](../vs140/CObArray--GetUpperBound.md).  
  
 *TYPE*  
 Type of the elements stored in the base-class array.  
  
 *ptr*  
 A pointer to the element to be inserted in the array at the nIndex. A NULL value is allowed.  
  
## Remarks  
 For more detailed remarks, see [CObArray::SetAt](../vs140/CObArray--SetAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrArray Class](../vs140/CTypedPtrArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)