---
title: "CMDIFrameWndEx::OnClosePopupMenu"
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
ms.assetid: 1fd83215-d43d-491c-9279-fd18af7751c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnClosePopupMenu
Called by the framework when an active pop-up menu processes a `WM_DESTROY` message.  
  
## Syntax  
  
```  
virtual void OnClosePopupMenu(  
   CMFCPopupMenu* pMenuPopup   
);  
```  
  
#### Parameters  
 [in] `pMenuPopup`  
 Pointer to a pop-up menu.  
  
## Remarks  
 Override this method if you want to process notifications from [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) objects that belong to the MDI frame window when those objects process `WM_DESTROY` messages.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)