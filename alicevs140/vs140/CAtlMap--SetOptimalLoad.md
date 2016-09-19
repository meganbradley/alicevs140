---
title: "CAtlMap::SetOptimalLoad"
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
ms.assetid: 1e110a1c-2b36-4753-b977-3cee25673b0b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::SetOptimalLoad
Call this method to set the optimal load of the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      void SetOptimalLoad(  
   float fOptimalLoad,  
   float fLoThreshold,  
   float fHiThreshold,  
   bool bRehashNow = false   
);  
```  
  
#### Parameters  
 `fOptimalLoad`  
 The optimal load ratio.  
  
 `fLoThreshold`  
 The lower threshold for the load ratio.  
  
 `fHiThreshold`  
 The upper threshold for the load ratio.  
  
 `bRehashNow`  
 Flag indicating if the hash table should be recalculated.  
  
## Remarks  
 This method redefines the optimal load value for the `CAtlMap` object. See [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md) for a discussion of the various parameters. If `bRehashNow` is true, and the number of elements is outside the minimum and maximum values, the hash table is recalculated.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)