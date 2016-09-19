---
title: "COleServerDoc::GetItemClipRect"
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
ms.assetid: 14bf50d1-0441-4649-b21f-56a3423ea50d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::GetItemClipRect
Call the `GetItemClipRect` member function to get the clipping-rectangle coordinates of the item that is being edited in place.  
  
## Syntax  
  
```  
  
      void GetItemClipRect(  
   LPRECT lpClipRect   
) const;  
```  
  
#### Parameters  
 `lpClipRect`  
 Pointer to a `RECT` structure or a `CRect` object to receive the clipping-rectangle coordinates of the item.  
  
## Remarks  
 Coordinates are in pixels relative to the container application window's client area.  
  
 Drawing should not occur outside the clipping rectangle. Usually, drawing is automatically restricted. Use this function to determine whether the user has scrolled outside the visible portion of the document; if so, scroll the container document as needed by means of a call to [ScrollContainerBy](../vs140/COleServerDoc--ScrollContainerBy.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::GetItemPosition](../vs140/COleServerDoc--GetItemPosition.md)   
 [COleServerDoc::ScrollContainerBy](../vs140/COleServerDoc--ScrollContainerBy.md)