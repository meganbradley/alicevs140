---
title: "CAtlMap::Rehash"
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
ms.assetid: 05dc2957-a10e-444c-8617-22cd2892142c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::Rehash
Call this method to rehash the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      void Rehash(  
   UINT nBins = 0   
);  
```  
  
#### Parameters  
 `nBins`  
 The new number of bins to use in the hash table. See [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md) for an explanation.  
  
## Remarks  
 If `nBins` is 0, `CAtlMap` calculates a reasonable number based on the number of elements in the map and the optimal load setting. Normally the rehashing process is automatic, but if [CAtlMap::DisableAutoRehash](../vs140/CAtlMap--DisableAutoRehash.md) has been called, this method will perform the necessary resizing.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)