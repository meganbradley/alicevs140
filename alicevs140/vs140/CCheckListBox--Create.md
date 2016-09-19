---
title: "CCheckListBox::Create"
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
ms.assetid: b46bc47a-e7a6-4e2e-ae54-368ec2c0b390
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::Create
Creates the Windows checklist box and attaches it to the `CCheckListBox` object.  
  
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
 Specifies the style of the checklist box. The style must be **LBS_HASSTRINGS** and either **LBS_OWNERDRAWFIXED** (all items in the list are the same height) or **LBS_OWNERDRAWVARIABLE** (items in the list are of varying heights). This style can be combined with other [list-box styles](../vs140/List-Box-Styles.md) except **LBS_USETABSTOPS**.  
  
 `rect`  
 Specifies the checklist-box size and position. Can be either a [CRect](../vs140/CRect-Class.md) object or a [RECT](../vs140/RECT-Structure.md) structure.  
  
 `pParentWnd`  
 Specifies the checklist box's parent window (usually a `CDialog` object). It must not be **NULL**.  
  
 `nID`  
 Specifies the checklist box's control ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You construct a `CCheckListBox` object in two steps. First, define a class derived from **CcheckListBox** and then call **Create**, which initializes the Windows checklist box and attaches it to the `CCheckListBox`. See [CCheckListBox::CCheckListBox](../vs140/CCheckListBox--CCheckListBox.md) for a sample.  
  
 When **Create** executes, Windows sends the [WM_NCCREATE](../vs140/CWnd--OnNcCreate.md), [WM_CREATE](../vs140/CWnd--OnCreate.md), [WM_NCCALCSIZE](../vs140/CWnd--OnNcCalcSize.md), and [WM_GETMINMAXINFO](../vs140/CWnd--OnGetMinMaxInfo.md) messages to the checklist-box control.  
  
 These messages are handled by default by the [OnNcCreate](../vs140/CWnd--OnNcCreate.md), [OnCreate](../vs140/CWnd--OnCreate.md), [OnNcCalcSize](../vs140/CWnd--OnNcCalcSize.md), and [OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md) member functions in the `CWnd` base class. To extend the default message handling, add a message map to the your derived class and override the preceding message-handler member functions. Override `OnCreate`, for example, to perform needed initialization for a new class.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to a checklist-box control:  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
-   **WS_VSCROLL** To add a vertical scroll bar  
  
-   **WS_HSCROLL** To add a horizontal scroll bar  
  
-   **WS_GROUP** To group controls  
  
-   **WS_TABSTOP** To allow tabbing to this control  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::CCheckListBox](../vs140/CCheckListBox--CCheckListBox.md)