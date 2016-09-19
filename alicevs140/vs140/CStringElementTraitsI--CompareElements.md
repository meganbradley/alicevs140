---
title: "CStringElementTraitsI::CompareElements"
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
ms.assetid: d1fbdcec-74d8-4c32-a11b-1b3985850fe8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringElementTraitsI::CompareElements
Call this static function to compare two string elements for equality, ignoring differences in case.  
  
## Syntax  
  
```  
  
      static bool CompareElements(  
   INARGTYPE str1,  
   INARGTYPE str2   
) throw( );  
```  
  
#### Parameters  
 `str1`  
 The first string element.  
  
 `str2`  
 The second string element.  
  
## Return Value  
 Returns true if the elements are equal, false otherwise.  
  
## Remarks  
 Comparisons are case insensitive.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CStringElementTraitsI Class](../vs140/CStringElementTraitsI-Class.md)   
 [CStringElementTraitsI::CompareElementsOrdered](../vs140/CStringElementTraitsI--CompareElementsOrdered.md)   
 [CStringElementTraits::CompareElements](../vs140/CStringElementTraits--CompareElements.md)