---
title: "CStringElementTraits::CompareElements"
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
ms.assetid: c47b5a5e-8729-4e2a-a104-0d06d1f7c98f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringElementTraits::CompareElements
Call this static function to compare two string elements for equality.  
  
## Syntax  
  
```  
  
      static bool CompareElements(  
   INARGTYPE str1,  
   INARGTYPE str2   
);  
```  
  
#### Parameters  
 `str1`  
 The first string element.  
  
 `str2`  
 The second string element.  
  
## Return Value  
 Returns true if the elements are equal, false otherwise.  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringElementTraits Class](../vs140/CStringElementTraits-Class.md)   
 [CStringElementTraits::CompareElementsOrdered](../vs140/CStringElementTraits--CompareElementsOrdered.md)   
 [CStringElementTraitsI::CompareElements](../vs140/CStringElementTraitsI--CompareElements.md)