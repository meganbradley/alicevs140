---
title: "CMFCTabCtrl::OnDragOver"
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
ms.assetid: a9eda309-f37d-485f-b6fc-1389f4746824
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::OnDragOver
Called by the framework during a drag operation when the mouse is moved over the drop target window.  
  
## Syntax  
  
```  
virtual DROPEFFECT OnDragOver(  
   COleDataObject* pDataObject,  
   DWORD dwKeyState,  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `pDataObject`  
 Pointer to a [COleDataObject](../vs140/COleDataObject-Class.md) object that is being dragged over the drop target.  
  
 [in] `dwKeyState`  
 The state of the modifier keys, which is a bitwise combination (OR) of `MK_CONTROL`, `MK_SHIFT`, `MK_ALT`, `MK_LBUTTON`, `MK_MBUTTON`, and `MK_RBUTTON`. For more information, see "Message Parameters" in [About Mouse Input](http://msdn.microsoft.com/library/windows/desktop/ms645601).  
  
 [in] `point`  
 The current mouse position.  
  
## Return Value  
 Always `DROPEFFECT_NONE`.  
  
## Remarks  
 Override this method with your custom implementation. For more information, see the [CView::OnDragOver](../vs140/CView--OnDragOver.md) method.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [About Mouse Input](http://msdn.microsoft.com/library/windows/desktop/ms645601)