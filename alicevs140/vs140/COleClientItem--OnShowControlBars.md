---
title: "COleClientItem::OnShowControlBars"
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
ms.assetid: c97fc6e3-16b4-43e8-ae3b-9d98a094ef71
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnShowControlBars
Called by the framework to show and hide the container application's control bars.  
  
## Syntax  
  
```  
  
      virtual BOOL OnShowControlBars(  
   CFrameWnd* pFrameWnd,  
   BOOL bShow   
);  
```  
  
#### Parameters  
 `pFrameWnd`  
 Pointer to the container application's frame window. This can be either a main frame window or an MDI child window.  
  
 `bShow`  
 Specifies whether control bars are to be shown or hidden.  
  
## Return Value  
 Nonzero if the function call causes a change in the control bars' state; 0 if the call causes no change, or if `pFrameWnd` does not point to the container's frame window.  
  
## Remarks  
 This function returns 0 if the control bars are already in the state specified by *bShow.* This would occur, for example, if the control bars are hidden and `bShow` is **FALSE**.  
  
 The default implementation removes the toolbar from the top-level frame window.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnInsertMenus](../vs140/COleClientItem--OnInsertMenus.md)   
 [COleClientItem::OnSetMenu](../vs140/COleClientItem--OnSetMenu.md)   
 [COleClientItem::OnRemoveMenus](../vs140/COleClientItem--OnRemoveMenus.md)   
 [COleClientItem::OnUpdateFrameTitle](../vs140/COleClientItem--OnUpdateFrameTitle.md)