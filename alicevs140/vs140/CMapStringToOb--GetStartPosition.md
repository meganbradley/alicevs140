---
title: "CMapStringToOb::GetStartPosition"
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
ms.assetid: 49a6382a-6505-450b-941d-35a15655d170
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::GetStartPosition
Starts a map iteration by returning a **POSITION** value that can be passed to a `GetNextAssoc` call.  
  
## Syntax  
  
```  
  
POSITION GetStartPosition( ) const;  
```  
  
## Return Value  
 A **POSITION** value that indicates a starting position for iterating the map; or **NULL** if the map is empty.  
  
## Remarks  
 The iteration sequence is not predictable; therefore, the "first element in the map" has no special significance.  
  
 The following table shows other member functions that are similar to `CMapStringToOb::GetStartPosition`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**POSITION GetStartPosition( ) const;**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**POSITION GetStartPosition( ) const;**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**POSITION GetStartPosition( ) const;**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**POSITION GetStartPosition( ) const;**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**POSITION GetStartPosition( ) const;**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**POSITION GetStartPosition( ) const;**|  
  
## Example  
 See the example for [CMapStringToOb::GetNextAssoc](../vs140/CMapStringToOb--GetNextAssoc.md).  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)