---
title: "COleServerDoc::GetZoomFactor"
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
ms.assetid: 7e01fd2d-9e2f-4663-a450-6ab244310e3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::GetZoomFactor
The `GetZoomFactor` member function determines the "zoom factor" of an item that has been activated for in-place editing.  
  
## Syntax  
  
```  
  
      BOOL GetZoomFactor(  
   LPSIZE lpSizeNum = NULL,  
   LPSIZE lpSizeDenom = NULL,  
   LPCRECT lpPosRect = NULL   
) const;  
```  
  
#### Parameters  
 *lpSizeNum*  
 Pointer to an object of class `CSize` that will hold the zoom factor's numerator. Can be **NULL**.  
  
 *lpSizeDenom*  
 Pointer to an object of class `CSize` that will hold the zoom factor's denominator. Can be **NULL**.  
  
 `lpPosRect`  
 Pointer to an object of class `CRect` that describes the item's new position. If this argument is **NULL**, the function uses the item's current position.  
  
## Return Value  
 Nonzero if the item is activated for in-place editing and its zoom factor is other than 100% (1:1); otherwise 0.  
  
## Remarks  
 The zoom factor, in pixels, is the proportion of the item's size to its current extent. If the container application has not set the item's extent, its natural extent (as determined by [COleServerItem::OnGetExtent](../vs140/COleServerItem--OnGetExtent.md)) is used.  
  
 The function sets its first two arguments to the numerator and denominator of the item's "zoom factor." If the item is not being edited in place, the function sets these arguments to a default value of 100% (or 1:1) and returns zero. For further information, see Technical Note 40, [MFC/OLE In-Place Resizing and Zooming](../vs140/TN040--MFC-OLE-In-Place-Resizing-and-Zooming.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::GetItemPosition](../vs140/COleServerDoc--GetItemPosition.md)   
 [COleServerDoc::GetItemClipRect](../vs140/COleServerDoc--GetItemClipRect.md)   
 [COleServerDoc::OnSetItemRects](../vs140/COleServerDoc--OnSetItemRects.md)