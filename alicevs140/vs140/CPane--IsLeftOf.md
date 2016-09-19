---
title: "CPane::IsLeftOf"
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
ms.assetid: e679baf2-eeee-4aca-a107-dc0d47bcc1d2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::IsLeftOf
Determines whether the pane is left of (or above) the specified rectangle.  
  
## Syntax  
  
```  
bool IsLeftOf(  
   CRect rect,  
   bool bWindowRect = true  
) const;  
```  
  
#### Parameters  
 [in] `rect`  
 A `CRect` object that is used for comparison.  
  
 [in] `bWindowRect`  
 If `TRUE`, `rect` is assumed to contain screen coordinates; if `FALSE`, `rect` is assumed to contain client coordinates.  
  
## Return Value  
  
## Remarks  
 If the pane is docked horizontally, this method checks whether its location is left of `rect`. Otherwise, this method checks whether the location is above `rect`.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)