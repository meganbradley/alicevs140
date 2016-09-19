---
title: "COleClientItem::GetInPlaceWindow"
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
ms.assetid: 884974cf-3ff6-459f-bc5d-7a0e91b45459
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetInPlaceWindow
Call the `GetInPlaceWindow` member function to get a pointer to the window in which the item has been opened for in-place editing.  
  
## Syntax  
  
```  
  
CWnd* GetInPlaceWindow( );  
```  
  
## Return Value  
 A pointer to the item's in-place editing window; **NULL** if the item is not active or if its server is unavailable.  
  
## Remarks  
 This function should be called only for items that are in-place active.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::Activate](../vs140/COleClientItem--Activate.md)   
 [COleClientItem::Deactivate](../vs140/COleClientItem--Deactivate.md)   
 [COleClientItem::SetItemRects](../vs140/COleClientItem--SetItemRects.md)