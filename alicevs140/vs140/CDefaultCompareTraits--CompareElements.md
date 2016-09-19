---
title: "CDefaultCompareTraits::CompareElements"
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
ms.assetid: 43852805-c07f-4a88-8307-e2295cf9e733
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDefaultCompareTraits::CompareElements
Call this function to compare two elements for equality.  
  
## Syntax  
  
```  
  
      static bool CompareElements(  
   const T& element1,  
   const T& element2   
);  
```  
  
#### Parameters  
 `element1`  
 The first element.  
  
 `element2`  
 The second element.  
  
## Return Value  
 Returns true if the elements are equal, false otherwise.  
  
## Remarks  
 The default implementation of this function is the equality (`==`) operator. For objects other than simple data types, this function may need to be overridden.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CDefaultCompareTraits Class](../vs140/CDefaultCompareTraits-Class.md)   
 [CDefaultCompareTraits::CompareElementsOrdered](../vs140/CDefaultCompareTraits--CompareElementsOrdered.md)