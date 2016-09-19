---
title: "CAtlMap::GetAt"
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
ms.assetid: 548a6457-5f25-4af6-87e3-a9327ee7e1bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetAt
Call this method to return the element at a specified position in the map.  
  
## Syntax  
  
```  
  
      void GetAt(  
   POSITION pos,  
   KOUTARGTYPE key,  
   VOUTARGTYPE value   
) const;  
CPair* GetAt(  
   POSITION& pos   
) throw( );  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
 `key`  
 Template parameter specifying the type of the map's key.  
  
 *value*  
 Template parameter specifying the type of the map's value.  
  
## Return Value  
 Returns a pointer to the current pair of key/value elements stored in the map.  
  
## Remarks  
 In debug builds, an assertion error will occur if `pos` is equal to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::SetAt](../vs140/CAtlMap--SetAt.md)   
 [CAtlMap::GetKeyAt](../vs140/CAtlMap--GetKeyAt.md)   
 [CAtlMap::GetValueAt](../vs140/CAtlMap--GetValueAt.md)   
 [CAtlMap::CPair Class](../vs140/CAtlMap--CPair-Class.md)