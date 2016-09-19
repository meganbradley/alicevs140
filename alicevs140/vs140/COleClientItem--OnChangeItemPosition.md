---
title: "COleClientItem::OnChangeItemPosition"
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
ms.assetid: b8101c64-3165-4488-833b-fee026d450be
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnChangeItemPosition
Called by the framework to notify the container that the OLE item's extent has changed during in-place activation.  
  
## Syntax  
  
```  
  
      virtual BOOL OnChangeItemPosition(  
   const CRect& rectPos   
);  
```  
  
#### Parameters  
 *rectPos*  
 Indicates the item's position relative to the container application's client area.  
  
## Return Value  
 Nonzero if the item's position is successfully changed; otherwise 0.  
  
## Remarks  
 The default implementation determines the new visible rectangle of the OLE item and calls [SetItemRects](../vs140/COleClientItem--SetItemRects.md) with the new values. The default implementation calculates the visible rectangle for the item and passes that information to the server.  
  
 Override this function to apply special rules to the resize/move operation. If the application is written in MFC, this call results because the server called [COleServerDoc::RequestPositionChange](../vs140/COleServerDoc--RequestPositionChange.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::RequestPositionChange](../vs140/COleServerDoc--RequestPositionChange.md)