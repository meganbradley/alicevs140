---
title: "CListBox::Create"
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
ms.assetid: e434b93c-7633-436b-b26c-bfec5c262116
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::Create
Creates the Windows list box and attaches it to the `CListBox` object.  
  
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
 Specifies the style of the list box. Apply any combination of [list-box styles](../vs140/List-Box-Styles.md) to the box.  
  
 `rect`  
 Specifies the list-box size and position. Can be either a `CRect` object or a `RECT` structure.  
  
 `pParentWnd`  
 Specifies the list box's parent window (usually a `CDialog` object). It must not be **NULL**.  
  
 `nID`  
 Specifies the list box's control ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You construct a `CListBox` object in two steps. First, call the constructor and then call **Create**, which initializes the Windows list box and attaches it to the `CListBox` object.  
  
 When **Create** executes, Windows sends the [WM_NCCREATE](../vs140/CWnd--OnNcCreate.md), [WM_CREATE](../vs140/CWnd--OnCreate.md), [WM_NCCALCSIZE](../vs140/CWnd--OnNcCalcSize.md), and [WM_GETMINMAXINFO](../vs140/CWnd--OnGetMinMaxInfo.md) messages to the list-box control.  
  
 These messages are handled by default by the [OnNcCreate](../vs140/CWnd--OnNcCreate.md), [OnCreate](../vs140/CWnd--OnCreate.md), [OnNcCalcSize](../vs140/CWnd--OnNcCalcSize.md), and [OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md) member functions in the `CWnd` base class. To extend the default message handling, derive a class from `CListBox`, add a message map to the new class, and override the preceding message-handler member functions. Override `OnCreate`, for example, to perform needed initialization for a new class.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to a list-box control.  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
-   **WS_VSCROLL** To add a vertical scroll bar  
  
-   **WS_HSCROLL** To add a horizontal scroll bar  
  
-   **WS_GROUP** To group controls  
  
-   **WS_TABSTOP** To allow tabbing to this control  
  
## Example  
 [!CODE [NVC_MFC_CListBox#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#2)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::CListBox](../vs140/CListBox--CListBox.md)