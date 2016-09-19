---
title: "CContainedWindowT::SubclassWindow"
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
ms.assetid: ddc92f81-79b2-4ec6-8d1f-78b7d4b47011
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::SubclassWindow
Subclasses the window identified by `hWnd` and attaches it to the `CContainedWindowT` object.  
  
## Syntax  
  
```  
  
      BOOL SubclassWindow(  
   HWND hWnd   
);  
```  
  
#### Parameters  
 `hWnd`  
 [in] The handle to the window being subclassed.  
  
## Return Value  
 **TRUE** if the window is successfully subclassed; otherwise, **FALSE**.  
  
## Remarks  
 The subclassed window now uses [CContainedWindowT::WindowProc](../vs140/CContainedWindowT--WindowProc.md). The original window procedure is saved in [m_pfnSuperWindowProc](../vs140/CContainedWindowT--m_pfnSuperWindowProc.md).  
  
> [!NOTE]
>  Do not call `SubclassWindow` if you have already called [Create](../vs140/CContainedWindowT--Create.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::UnsubclassWindow](../vs140/CContainedWindowT--UnsubclassWindow.md)