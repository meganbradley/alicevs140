---
title: "CElementTraitsBase::RelocateElements"
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
ms.assetid: b3270301-9642-4a8d-a6b8-f2557091c13d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CElementTraitsBase::RelocateElements
Call this method to relocate elements stored in a collection class object.  
  
## Syntax  
  
```  
  
      static void RelocateElements(  
   T* pDest,  
   T* pSrc,  
   size_t nElements   
);  
```  
  
#### Parameters  
 `pDest`  
 Pointer to the first element that will receive the relocated data.  
  
 `pSrc`  
 Pointer to the first element to relocate.  
  
 `nElements`  
 The number of elements to relocate.  
  
## Remarks  
 This method calls [memmove](../vs140/memmove--wmemmove.md), which is sufficient for most data types. If the objects being moved contain pointers to their own members, this method will need to be overridden.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CElementTraitsBase Class](../vs140/CElementTraitsBase-Class.md)   
 [CElementTraitsBase::CopyElements](../vs140/CElementTraitsBase--CopyElements.md)