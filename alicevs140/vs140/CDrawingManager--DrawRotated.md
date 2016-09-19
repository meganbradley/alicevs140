---
title: "CDrawingManager::DrawRotated"
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
ms.assetid: cd221bdb-351f-4911-8a93-7485448808c8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::DrawRotated
Rotates a source DC content inside the given rectangle by 90 degrees.  
  
## Syntax  
  
```  
void DrawRotated(  
   CRect rectDest,  
   CDC& dcSrc,  
   BOOL bClockWise  
);  
```  
  
#### Parameters  
 `rectDest`  
 Destination rectangle.  
  
 `dcSrc`  
 The source device context.  
  
 `bClockWise`  
 `TRUE` indicates rotate +90 degrees; `FALSE` indicates rotate -90 degrees.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)