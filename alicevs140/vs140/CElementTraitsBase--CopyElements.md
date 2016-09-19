---
title: "CElementTraitsBase::CopyElements"
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
ms.assetid: 54ed6e15-8653-4bae-9034-268ae1e4dbd6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CElementTraitsBase::CopyElements
Call this method to copy elements stored in a collection class object.  
  
## Syntax  
  
```  
  
      static void CopyElements(  
   T* pDest,  
   const T* pSrc,  
   size_t nElements   
);  
```  
  
#### Parameters  
 `pDest`  
 Pointer to the first element that will receive the copied data.  
  
 `pSrc`  
 Pointer to the first element to copy.  
  
 `nElements`  
 The number of elements to copy.  
  
## Remarks  
 The source and destination elements should not overlap.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CElementTraitsBase Class](../vs140/CElementTraitsBase-Class.md)   
 [CElementTraitsBase::RelocateElements](../vs140/CElementTraitsBase--RelocateElements.md)