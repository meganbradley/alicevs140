---
title: "COleDocument::GetInPlaceActiveItem"
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
ms.assetid: 6e29f6b2-9cb6-41dc-a824-92a022df0bd0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::GetInPlaceActiveItem
Call this function to get the OLE item that is currently activated in place in the frame window containing the view identified by `pWnd`.  
  
## Syntax  
  
```  
  
      virtual COleClientItem* GetInPlaceActiveItem(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Pointer to the window that displays the container document.  
  
## Return Value  
 A pointer to the single, in-place active OLE item; **NULL** if there is no OLE item currently in the "in-place active" state.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)