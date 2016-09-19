---
title: "COleServerDoc::GetItemPosition"
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
ms.assetid: d7bddf7d-ec7a-4bb3-b4f8-d7eeb3306ef9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::GetItemPosition
Call the `GetItemPosition` member function to get the coordinates of the item being edited in place.  
  
## Syntax  
  
```  
  
      void GetItemPosition(  
   LPRECT lpPosRect   
) const;  
```  
  
#### Parameters  
 `lpPosRect`  
 Pointer to a `RECT` structure or a `CRect` object to receive the coordinates of the item.  
  
## Remarks  
 Coordinates are in pixels relative to the container application window's client area.  
  
 The item's position can be compared with the current clipping rectangle to determine the extent to which the item is visible (or not visible) on the screen.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::GetItemClipRect](../vs140/COleServerDoc--GetItemClipRect.md)