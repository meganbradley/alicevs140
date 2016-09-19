---
title: "CAtlMap::SetValueAt"
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
ms.assetid: 1360be45-f32c-4bda-a54a-6bd691e3c1ef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::SetValueAt
Call this method to change the value stored at a given position in the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      void SetValueAt(  
   POSITION pos,  
   VINARGTYPE value   
);  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
 *value*  
 The value to add to the `CAtlMap` object.  
  
## Remarks  
 Changes the value element stored at the given position in the `CAtlMap` object.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::SetAt](../vs140/CAtlMap--SetAt.md)   
 [CAtlMap::GetKeyAt](../vs140/CAtlMap--GetKeyAt.md)