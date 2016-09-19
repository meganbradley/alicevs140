---
title: "CAtlMap::GetNextAssoc"
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
ms.assetid: d4cb97c8-c446-4b63-9507-9518f16a9f97
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetNextAssoc
Gets the next element for iterating.  
  
## Syntax  
  
```  
  
      void GetNextAssoc(  
   POSITION& pos,  
   KOUTARGTYPE key,  
   VOUTARGTYPE value   
) const;  
```  
  
#### Parameters  
 `pos`  
 The position counter, returned by a previous call to [CAtlMap::GetNextAssoc](#vclrfcatlmapgetnextassoc) or [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md).  
  
 `key`  
 Template parameter specifying the type of the map's key.  
  
 *value*  
 Template parameter specifying the type of the map's value.  
  
## Remarks  
 The `pos` position counter is updated after each call. If the retrieved element is the last in the map, `pos` is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::GetNext](../vs140/CAtlMap--GetNext.md)   
 [CAtlMap::GetNextKey](../vs140/CAtlMap--GetNextKey.md)   
 [CAtlMap::GetNextValue](../vs140/CAtlMap--GetNextValue.md)   
 [CAtlMap::GetStartPosition](../vs140/CAtlMap--GetStartPosition.md)