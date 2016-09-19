---
title: "CMFCTabDropTarget::OnDropEx"
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
ms.assetid: 4c337872-abaf-4fda-82bb-a9b2ab89ed4b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabDropTarget::OnDropEx
Called by the framework when the user releases the mouse button at the end of a drag operation.  
  
## Syntax  
  
```  
virtual DROPEFFECT OnDropEx(  
   CWnd* pWnd,  
   COleDataObject* pDataObject,  
   DROPEFFECT dropEffect,  
   DROPEFFECT dropList,  
   CPoint point  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pWnd`|Unused.|  
|[in] `pDataObject`|A pointer to the object that the user drags.|  
|[in] `dropEffect`|The default drop operation.|  
|[in] `dropList`|Unused.|  
|[in] `point`|The location of the mouse pointer in client coordinates.|  
  
## Return Value  
 The resulting drop effect. It can be one or more of the following:  
  
-   `DROPEFFECT_NONE`  
  
-   `DROPEFFECT_COPY`  
  
-   `DROPEFFECT_MOVE`  
  
-   `DROPEFFECT_LINK`  
  
-   `DROPEFFECT_SCROLL`  
  
## Remarks  
 This method calls `CMFCBaseTabCtrl::OnDrop` if the toolbar framework is in customization mode and the Clipboard data format is available. If the call to `CMFCBaseTabCtrl::OnDrop` returns a nonzero value, this method returns the default drop effect specified by `dropEffect`. Otherwise, this method returns `DROPEFFECT_NONE`. For more information about drop effects, see [COleDropTarget::OnDropEx](../vs140/COleDropTarget--OnDropEx.md).  
  
 For more information about customization mode, see [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md). For more information about Clipboard data formats, see [COleDataObject::IsDataAvailable](../vs140/COleDataObject--IsDataAvailable.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCTabDropTarget Class](../vs140/CMFCTabDropTarget-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [COleDropTarget::OnDropEx](../vs140/COleDropTarget--OnDropEx.md)   
 [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md)   
 [COleDataObject::IsDataAvailable](../vs140/COleDataObject--IsDataAvailable.md)