---
title: "CAtlArray::SetCount"
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
ms.assetid: 1212bd03-5ec1-4980-a2c9-15a80ed256a4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::SetCount
Call this method to set the size of the array object.  
  
## Syntax  
  
```  
  
      bool SetCount(  
   size_t nNewSize,  
   int nGrowBy = - 1   
);  
```  
  
#### Parameters  
 `nNewSize`  
 The required size of the array.  
  
 `nGrowBy`  
 A value used to determine how large to make the buffer. A value of -1 causes an internally calculated value to be used.  
  
## Return Value  
 Returns true if the array is successfully resized, false otherwise.  
  
## Remarks  
 The array can be increased or decreased in size. If increased, extra empty elements are added to the array. If decreased, the elements with the largest indices will be deleted and memory freed.  
  
 Use this method to set the size of the array before using it. If `SetCount` is not used, the process of adding elements — and the subsequent memory allocation performed — will reduce performance and fragment memory.  
  
## Example  
 See the example for [CAtlArray::GetData](../vs140/CAtlArray--GetData.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)