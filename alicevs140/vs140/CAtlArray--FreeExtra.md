---
title: "CAtlArray::FreeExtra"
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
ms.assetid: ef490308-43a8-4660-ba25-96aee8f91581
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::FreeExtra
Call this method to remove any empty elements from the array.  
  
## Syntax  
  
```  
  
void FreeExtra( ) throw( );  
  
```  
  
## Remarks  
 Any empty elements are removed, but the size and upper bound of the array remain unchanged.  
  
 In debug builds, an ATLASSERT will be raised if the CAtlArray object is not valid, or if the array would exceed its maximum size.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::RemoveAll](../vs140/CAtlArray--RemoveAll.md)