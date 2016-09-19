---
title: "CArray::SetSize"
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
ms.assetid: fcb31f5b-2aa5-4251-97b7-f00557e08592
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::SetSize
Establishes the size of an empty or existing array; allocates memory if necessary.  
  
## Syntax  
  
```  
  
      void SetSize(  
   INT_PTR nNewSize,  
   INT_PTR nGrowBy = -1   
);  
```  
  
#### Parameters  
 `nNewSize`  
 The new array size (number of elements). Must be greater than or equal to 0.  
  
 `nGrowBy`  
 The minimum number of element slots to allocate if a size increase is necessary.  
  
## Remarks  
 If the new size is smaller than the old size, then the array is truncated and all unused memory is released.  
  
 Use this function to set the size of your array before you begin using the array. If you do not use `SetSize`, adding elements to your array causes it to be frequently reallocated and copied. Frequent reallocation and copying are inefficient and can fragment memory.  
  
 The `nGrowBy` parameter affects internal memory allocation while the array is growing. Its use never affects the array size as reported by [GetSize](../vs140/CArray--GetSize.md) and [GetUpperBound](../vs140/CArray--GetUpperBound.md). If the default value is used, MFC allocates memory in a way calculated to avoid memory fragmentation and optimize efficiency for most cases.  
  
## Example  
 See the example for [GetData](../vs140/CArray--GetData.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetUpperBound](../vs140/CArray--GetUpperBound.md)   
 [CArray::GetSize](../vs140/CArray--GetSize.md)   
 [CArray::GetCount](../vs140/CArray--GetCount.md)