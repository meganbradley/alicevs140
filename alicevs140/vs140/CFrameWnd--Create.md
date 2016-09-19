---
title: "CFrameWnd::Create"
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
ms.assetid: d3d3bb87-c1e5-450f-b09d-2867a3c8438f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::Create
Call to create and initialize the Windows frame window associated with the `CFrameWnd` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   LPCTSTR lpszClassName,  
   LPCTSTR lpszWindowName,  
   DWORD dwStyle = WS_OVERLAPPEDWINDOW,  
   const RECT& rect = rectDefault,  
   CWnd* pParentWnd = NULL,  
   LPCTSTR lpszMenuName = NULL,  
   DWORD dwExStyle = 0,  
   CCreateContext* pContext = NULL   
);  
```  
  
#### Parameters  
 `lpszClassName`  
 Points to a null-terminated character string that names the Windows class. The class name can be any name registered with the `AfxRegisterWndClass` global function or the **RegisterClass** Windows function. If **NULL**, uses the predefined default `CFrameWnd` attributes.  
  
 `lpszWindowName`  
 Points to a null-terminated character string that represents the window name. Used as text for the title bar.  
  
 `dwStyle`  
 Specifies the window [style](../vs140/Window-Styles.md) attributes. Include the **FWS_ADDTOTITLE** style if you want the title bar to automatically display the name of the document represented in the window.  
  
 `rect`  
 Specifies the size and position of the window. The `rectDefault` value allows Windows to specify the size and position of the new window.  
  
 `pParentWnd`  
 Specifies the parent window of this frame window. This parameter should be **NULL** for top-level frame windows.  
  
 *lpszMenuName*  
 Identifies the name of the menu resource to be used with the window. Use **MAKEINTRESOURCE** if the menu has an integer ID instead of a string. This parameter can be **NULL**.  
  
 `dwExStyle`  
 Specifies the window extended [style](../vs140/Extended-Window-Styles.md) attributes.  
  
 `pContext`  
 Specifies a pointer to a [CCreateContext](../vs140/CCreateContext-Structure.md) structure. This parameter can be **NULL**.  
  
## Return Value  
 Nonzero if initialization is successful; otherwise 0.  
  
## Remarks  
 Construct a `CFrameWnd` object in two steps. First, invoke the constructor, which constructs the `CFrameWnd` object, and then call **Create**, which creates the Windows frame window and attaches it to the `CFrameWnd` object. **Create** initializes the window's class name and window name and registers default values for its style, parent, and associated menu.  
  
 Use `LoadFrame` rather than **Create** to load the frame window from a resource instead of specifying its arguments.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::CFrameWnd](../vs140/CFrameWnd--CFrameWnd.md)   
 [CFrameWnd::LoadFrame](../vs140/CFrameWnd--LoadFrame.md)   
 [CCreateContext Structure](../vs140/CCreateContext-Structure.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWnd::PreCreateWindow](../vs140/CWnd--PreCreateWindow.md)