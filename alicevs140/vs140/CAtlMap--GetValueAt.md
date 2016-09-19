---
title: "CAtlMap::GetValueAt"
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
ms.assetid: d357c4c8-917e-46ad-8ac6-6623b76130c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetValueAt
Call this method to retrieve the value stored at a given position in the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      V& GetValueAt(  
   POSITION pos   
) throw( );  
const V& GetValueAt(  
   POSITION pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
## Return Value  
 Returns a reference to the value stored at the given position in the `CAtlMap` object.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::SetValueAt](../vs140/CAtlMap--SetValueAt.md)