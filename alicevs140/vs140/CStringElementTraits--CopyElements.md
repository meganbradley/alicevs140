---
title: "CStringElementTraits::CopyElements"
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
ms.assetid: e92a0321-bcba-4c77-898d-aeae95918d34
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringElementTraits::CopyElements
Call this static function to copy `CString` elements stored in a collection class object.  
  
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
 **Header:** cstringt.h  
  
## See Also  
 [CStringElementTraits Class](../vs140/CStringElementTraits-Class.md)   
 [CStringElementTraits::RelocateElements](../vs140/CStringElementTraits--RelocateElements.md)