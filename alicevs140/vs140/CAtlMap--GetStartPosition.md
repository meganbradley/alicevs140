---
title: "CAtlMap::GetStartPosition"
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
ms.assetid: 200586d6-7b83-4952-a681-676c7fd120e5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::GetStartPosition
Call this method to start a map iteration.  
  
## Syntax  
  
```  
  
POSITION GetStartPosition( ) const throw( );  
  
```  
  
## Return Value  
 Returns the start position, or NULL is returned if the map is empty.  
  
## Remarks  
 Call this method to start a map iteration by returning a **POSITION** value that can be passed to the `GetNextAssoc` method.  
  
> [!NOTE]
>  The iteration sequence is not predictable  
  
## Example  
 See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::GetNextAssoc](../vs140/CAtlMap--GetNextAssoc.md)