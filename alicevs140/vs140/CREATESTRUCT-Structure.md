---
title: "CREATESTRUCT Structure"
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
ms.topic: article
ms.assetid: 028c7b5e-4fdc-48da-a550-d3e4f9e6cc85
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CREATESTRUCT Structure
The `CREATESTRUCT` structure defines the initialization parameters passed to the window procedure of an application.  
  
## Syntax  
  
```  
  
      typedef struct tagCREATESTRUCT {  
   LPVOID lpCreateParams;  
   HANDLE hInstance;  
   HMENU hMenu;  
   HWND hwndParent;  
   int cy;  
   int cx;  
   int y;  
   int x;  
   LONG style;  
   LPCSTR lpszName;  
   LPCSTR lpszClass;  
   DWORD dwExStyle;  
} CREATESTRUCT;  
```  
  
#### Parameters  
 `lpCreateParams`  
 Points to data to be used to create the window.  
  
 `hInstance`  
 Identifies the module-instance handle of the module that owns the new window.  
  
 `hMenu`  
 Identifies the menu to be used by the new window. If a child window, contains the integer ID.  
  
 `hwndParent`  
 Identifies the window that owns the new window. This member is **NULL** if the new window is a top-level window.  
  
 `cy`  
 Specifies the height of the new window.  
  
 `cx`  
 Specifies the width of the new window.  
  
 `y`  
 Specifies the y-coordinate of the upper left corner of the new window. Coordinates are relative to the parent window if the new window is a child window; otherwise coordinates are relative to the screen origin.  
  
 `x`  
 Specifies the x-coordinate of the upper left corner of the new window. Coordinates are relative to the parent window if the new window is a child window; otherwise coordinates are relative to the screen origin.  
  
 `style`  
 Specifies the new window's [style](../vs140/Styles-Used-by-MFC.md).  
  
 `lpszName`  
 Points to a null-terminated string that specifies the new window's name.  
  
 `lpszClass`  
 Points to a null-terminated string that specifies the new window's Windows class name (a [WNDCLASS](http://msdn.microsoft.com/library/windows/desktop/ms633576) structure; for more information, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]).  
  
 `dwExStyle`  
 Specifies the [extended style](../vs140/Extended-Window-Styles.md) for the new window.  
  
## Requirements  
 **Header:** winuser.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CWnd::OnCreate](../vs140/CWnd--OnCreate.md)