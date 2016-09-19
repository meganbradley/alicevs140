---
title: "CAtlMap::GetKeyAt"
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
ms.assetid: 5c49dc7c-66ee-49cf-ae9f-4262bfbe83f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetKeyAt
Call this method to retrieve the key stored at the given position in the `CAtlMap` object.  
  
## Syntax  
  
```  
  
      const K& GetKeyAt(  
   POSITION pos   
) const throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
## Return Value  
 Returns a reference to the key stored at the given position in the `CAtlMap` object.  
  
## Example  
 See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::SetValueAt](../vs140/CAtlMap--SetValueAt.md)