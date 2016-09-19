---
title: "CSimpleMap::SetAtIndex"
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
ms.assetid: 53fd21f0-9c70-429c-98d0-bf7bbce66e84
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::SetAtIndex
Sets the key and value at a specified index.  
  
## Syntax  
  
```  
  
      BOOL SetAtIndex(  
   int nIndex,  
   const TKey& key,  
   const TVal& val   
);  
```  
  
#### Parameters  
 `nIndex`  
 The index, referencing the key and value pairing to change.  
  
 `key`  
 The new key.  
  
 *val*  
 The new value.  
  
## Return Value  
 Returns TRUE if successful, FALSE if the index was not valid.  
  
## Remarks  
 Updates both the key and value pointed to by `nIndex`.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::SetAt](../vs140/CSimpleMap--SetAt.md)