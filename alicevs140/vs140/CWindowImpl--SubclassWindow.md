---
title: "CWindowImpl::SubclassWindow"
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
ms.assetid: 62ebbca3-fa81-4a2e-bf90-1dc309d53dab
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::SubclassWindow
Subclasses the window identified by `hWnd` and attaches it to the `CWindowImpl` object.  
  
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
 The subclassed window now uses [CWindowImpl::WindowProc](../vs140/CWindowImpl--WindowProc.md). The original window procedure is saved in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md).  
  
> [!NOTE]
>  Do not call `SubclassWindow` if you have already called [Create](../vs140/CWindowImpl--Create.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)   
 [CWindowImpl::UnsubclassWindow](../vs140/CWindowImpl--UnsubclassWindow.md)