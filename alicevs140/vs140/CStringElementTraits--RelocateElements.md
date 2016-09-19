---
title: "CStringElementTraits::RelocateElements"
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
ms.assetid: 63b2bac1-511d-4d00-9077-8e80170cb65f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringElementTraits::RelocateElements
Call this static function to relocate `CString` elements stored in a collection class object.  
  
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
 This static function calls [memmove](../vs140/memmove--wmemmove.md), which is sufficient for most data types. If the objects being moved contain pointers to their own members, this static function will need to be overridden.  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringElementTraits Class](../vs140/CStringElementTraits-Class.md)   
 [CStringElementTraits::CopyElements](../vs140/CStringElementTraits--CopyElements.md)