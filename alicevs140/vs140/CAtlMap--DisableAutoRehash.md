---
title: "CAtlMap::DisableAutoRehash"
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
ms.assetid: ff0ae980-723d-45cd-af5e-59fff69041b9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::DisableAutoRehash
Call this method to disable automatic rehashing of the `CAtlMap` object.  
  
## Syntax  
  
```  
  
void DisableAutoRehash( ) throw( );  
  
```  
  
## Remarks  
 When automatic rehashing is enabled (which it is by default), the number of bins in the hash table will automatically be recalculated if the load value (the ratio of the number of bins to the number of elements stored in the array) exceeds the maximum or minimum values specified at the time the map was created.  
  
 `DisableAutoRehash` is most useful when a large number of elements will be added to the map at once. Instead of triggering the rehashing process every time the limits are exceeded, it is more efficient to call `DisableAutoRehash`, add the elements, and finally call [CAtlMap::EnableAutoRehash](../vs140/CAtlMap--EnableAutoRehash.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::EnableAutoRehash](../vs140/CAtlMap--EnableAutoRehash.md)