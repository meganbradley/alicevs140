---
title: "CMDIChildWnd::Create"
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
ms.assetid: a787e216-a447-4ae7-9508-23cccf52afcc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWnd::Create
Call this member function to create a Windows MDI child window and attach it to the `CMDIChildWnd` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   LPCTSTR lpszClassName,  
   LPCTSTR lpszWindowName,  
   DWORD dwStyle = WS_CHILD | WS_VISIBLE | WS_OVERLAPPEDWINDOW,  
   const RECT& rect = rectDefault,  
   CMDIFrameWnd* pParentWnd = NULL,  
   CCreateContext* pContext = NULL   
);  
```  
  
#### Parameters  
 `lpszClassName`  
 Points to a null-terminated character string that names the Windows class (a [WNDCLASS](http://msdn.microsoft.com/library/windows/desktop/ms633576) structure). The class name can be any name registered with the [AfxRegisterWndClass](../vs140/AfxRegisterWndClass.md) global function. Should be **NULL** for a standard `CMDIChildWnd`.  
  
 `lpszWindowName`  
 Points to a null-terminated character string that represents the window name. Used as text for the title bar.  
  
 `dwStyle`  
 Specifies the window [style](../vs140/Window-Styles.md) attributes. The **WS_CHILD** style is required.  
  
 `rect`  
 Contains the size and position of the window. The `rectDefault` value allows Windows to specify the size and position of the new `CMDIChildWnd`.  
  
 `pParentWnd`  
 Specifies the window's parent. If **NULL**, the main application window is used.  
  
 `pContext`  
 Specifies a [CCreateContext](../vs140/CCreateContext-Structure.md) structure. This parameter can be **NULL**.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The currently active MDI child frame window can determine the caption of the parent frame window. This feature is disabled by turning off the **FWS_ADDTOTITLE** style bit of the child frame window.  
  
 The framework calls this member function in response to a user command to create a child window, and the framework uses the `pContext` parameter to properly connect the child window to the application. When you call **Create**, `pContext` can be **NULL**.  
  
## Example  
 Example 1:  
  
 [!CODE [NVC_MFCWindowing#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#7)]  
  
## Example  
 Example 2:  
  
 [!CODE [NVC_MFCWindowing#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#8)]  
  
 [!CODE [NVC_MFCWindowing#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#9)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIChildWnd::CMDIChildWnd](../vs140/CMDIChildWnd--CMDIChildWnd.md)   
 [CWnd::PreCreateWindow](../vs140/CWnd--PreCreateWindow.md)