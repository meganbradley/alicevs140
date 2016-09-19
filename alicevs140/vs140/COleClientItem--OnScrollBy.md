---
title: "COleClientItem::OnScrollBy"
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
ms.assetid: b151bf79-536b-4d45-a937-af3a0579f420
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnScrollBy
Called by the framework to scroll the OLE item in response to requests from the server.  
  
## Syntax  
  
```  
  
      virtual BOOL OnScrollBy(  
   CSize sizeExtent   
);  
```  
  
#### Parameters  
 *sizeExtent*  
 Specifies the distances, in pixels, to scroll in the x and y directions.  
  
## Return Value  
 Nonzero if the item was scrolled; 0 if the item could not be scrolled.  
  
## Remarks  
 For example, if the OLE item is partially visible and the user moves outside the visible region while performing in-place editing, this function is called to keep the cursor visible. The default implementation does nothing. Override this function to scroll the item by the specified amount. Note that as a result of scrolling, the visible portion of the OLE item can change. Call [SetItemRects](../vs140/COleClientItem--SetItemRects.md) to update the item's visible rectangle.  
  
 For more information, see [IOleInPlaceSite::Scroll](http://msdn.microsoft.com/library/windows/desktop/ms690291) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::SetItemRects](../vs140/COleClientItem--SetItemRects.md)