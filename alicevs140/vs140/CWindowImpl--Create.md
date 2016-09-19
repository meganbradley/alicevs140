---
title: "CWindowImpl::Create"
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
ms.assetid: 86587c87-55aa-47c9-b333-bef30914143d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::Create
Creates a window based on a new window class.  
  
## Syntax  
  
```  
  
      HWND Create(  
   HWND hWndParent,  
   _U_RECT rect = NULL,  
   LPCTSTR szWindowName = NULL,  
   DWORD dwStyle = 0,  
   DWORD dwExStyle = 0,  
   _U_MENUorID MenuOrID = 0U,  
   LPVOID lpCreateParam = NULL  
);  
```  
  
#### Parameters  
 `hWndParent`  
 [in] The handle to the parent or owner window.  
  
 `rect`  
 [in] A [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure specifying the position of the window. The `RECT` can be passed by pointer or by reference.  
  
 `szWindowName`  
 [in] Specifies the name of the window. The default value is **NULL**.  
  
 `dwStyle`  
 [in] The style of the window. This value is combined with the style provided by the traits class for the window. The default value gives the traits class full control over the style. For a list of possible values, see [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `dwExStyle`  
 [in] The extended window style. This value is combined with the style provided by the traits class for the window. The default value gives the traits class full control over the style. For a list of possible values, see [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `MenuOrID`  
 [in] For a child window, the window identifier. For a top-level window, a menu handle for the window. The default value is **0U**.  
  
 `lpCreateParam`  
 [in] A pointer to window-creation data. For a full description, see the description for the final parameter to [CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680).  
  
## Return Value  
 If successful, the handle to the newly created window. Otherwise, **NULL**.  
  
## Remarks  
 **Create** first registers the window class if it has not yet been registered. The newly created window is automatically attached to the `CWindowImpl` object.  
  
> [!NOTE]
>  Do not call **Create** if you have already called [SubclassWindow](../vs140/CWindowImpl--SubclassWindow.md).  
  
 To use a window class that is based on an existing window class, derive your class from `CWindowImpl` and include the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro. The existing window class's window procedure is saved in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md). For more information, see the [CWindowImpl](../vs140/CWindowImpl-Class.md) overview.  
  
> [!NOTE]
>  If 0 is used as the value for the `MenuOrID` parameter, it must be specified as 0U (the default value) to avoid a compiler error.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)   
 [CWindowImpl::GetWndClassInfo](../vs140/CWindowImpl--GetWndClassInfo.md)   
 [CWndClassInfo::Register](../vs140/CWndClassInfo--Register.md)   
 [CWindow::m_hWnd](../vs140/CWindow--m_hWnd.md)