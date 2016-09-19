---
title: "CTypedPtrMap::Lookup"
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
ms.assetid: 1c2d1497-de52-4a94-9de6-49c998c80517
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTypedPtrMap::Lookup
`Lookup` uses a hashing algorithm to quickly find the map element with a key that matches exactly.  
  
## Syntax  
  
```  
  
      BOOL Lookup(  
   BASE_CLASS::BASE_ARG_KEY key,  
   VALUE& rValue   
) const;  
```  
  
#### Parameters  
 `BASE_CLASS`  
 Template parameter specifying the base class of this map's class.  
  
 `key`  
 The key of the element to be looked up.  
  
 *VALUE*  
 Template parameter specifying the type of values stored in this map.  
  
 `rValue`  
 Specifies the returned value of the retrieved element.  
  
## Return Value  
 Nonzero if the element was found; otherwise 0.  
  
## Remarks  
 This inline function calls `BASE_CLASS`**::Lookup**.  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CTypedPtrMap Class](../vs140/CTypedPtrMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMapStringToOb::Lookup](../vs140/CMapStringToOb--Lookup.md)