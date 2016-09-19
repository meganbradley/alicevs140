---
title: "CArray::RelocateElements"
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
ms.assetid: 0bacb202-afe6-4ca6-9160-3f3acf19cf74
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::RelocateElements
Relocates data to a new buffer when the array should grow or shrink.  
  
## Syntax  
  
```  
template<class TYPE, class ARG_TYPE>   
AFX_INLINE void CArray<TYPE, ARG_TYPE>::RelocateElements(   
   TYPE* pNewData,  
   const TYPE* pData,  
   INT_PTR nCount   
);  
```  
  
#### Parameters  
 `pNewData`  
 A new buffer for the array of elements.  
  
 `pData`  
 The old array of elements.  
  
 `nCount`  
 Number of elements in the old array.  
  
## Remarks  
 `pNewData` is always large enough to hold all the `pData` elements.  
  
 The [CArray](../vs140/CArray-Class.md) implementation uses this method to copy the old data to a new buffer when the array should grow or shrink (when [SetSize](../vs140/CArray--SetSize.md) or [FreeExtra](../vs140/CArray--FreeExtra.md) are called). The default implementation just copies the data.  
  
 For arrays in which an element contains a pointer to one of its own members, or another structure contains a pointer to one of the array elements, the pointers are not updated in plain copy. In this case, you can correct pointers by implementing a specialization of `RelocateElements` with the relevant types. You are also responsible for data copying.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray::SetSize](../vs140/CArray--SetSize.md)   
 [CArray::FreeExtra](../vs140/CArray--FreeExtra.md)