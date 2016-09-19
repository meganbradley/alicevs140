---
title: "CEdit::Create"
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
ms.assetid: c0b0c36c-d27d-48f5-92d8-e9ed9fad1261
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::Create
Creates the Windows edit control and attaches it to the `CEdit` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Specifies the edit control's style. Apply any combination of [edit styles](../vs140/Edit-Styles.md) to the control.  
  
 `rect`  
 Specifies the edit control's size and position. Can be a `CRect` object or `RECT` structure.  
  
 `pParentWnd`  
 Specifies the edit control's parent window (usually a `CDialog`). It must not be **NULL**.  
  
 `nID`  
 Specifies the edit control's ID.  
  
## Return Value  
 Nonzero if initialization is successful; otherwise 0.  
  
## Remarks  
 You construct a `CEdit` object in two steps. First, call the `CEdit` constructor and then call **Create**, which creates the Windows edit control and attaches it to the `CEdit` object.  
  
 When **Create** executes, Windows sends the [WM_NCCREATE](http://msdn.microsoft.com/library/windows/desktop/ms632635), [WM_NCCALCSIZE](http://msdn.microsoft.com/library/windows/desktop/ms632634), [WM_CREATE](http://msdn.microsoft.com/library/windows/desktop/ms632619), and [WM_GETMINMAXINFO](http://msdn.microsoft.com/library/windows/desktop/ms632626) messages to the edit control.  
  
 These messages are handled by default by the [OnNcCreate](../vs140/CWnd--OnNcCreate.md), [OnNcCalcSize](../vs140/CWnd--OnNcCalcSize.md), [OnCreate](../vs140/CWnd--OnCreate.md), and [OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md) member functions in the `CWnd` base class. To extend the default message handling, derive a class from `CEdit`, add a message map to the new class, and override the above message-handler member functions. Override `OnCreate`, for example, to perform needed initialization for the new class.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to an edit control.  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
-   **WS_GROUP** To group controls  
  
-   **WS_TABSTOP** To include edit control in the tabbing order  
  
## Example  
 [!CODE [NVC_MFC_CEdit#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#2)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::CEdit](../vs140/CEdit--CEdit.md)