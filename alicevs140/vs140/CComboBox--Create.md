---
title: "CComboBox::Create"
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
ms.assetid: 4886d704-7054-4ea4-b8d1-fd55d0500cf2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::Create
Creates the combo box and attaches it to the `CComboBox` object.  
  
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
 Specifies the style of the combo box. Apply any combination of [combo-box styles](../vs140/Combo-Box-Styles.md) to the box.  
  
 `rect`  
 Points to the position and size of the combo box. Can be a [RECT](../vs140/RECT-Structure.md) structure or a `CRect` object.  
  
 `pParentWnd`  
 Specifies the combo box's parent window (usually a `CDialog`). It must not be **NULL**.  
  
 `nID`  
 Specifies the combo box's control ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You construct a `CComboBox` object in two steps. First, call the constructor and then call **Create**, which creates the Windows combo box and attaches it to the `CComboBox` object.  
  
 When **Create** executes, Windows sends the [WM_NCCREATE](../vs140/CWnd--OnNcCreate.md), [WM_CREATE](../vs140/CWnd--OnCreate.md), [WM_NCCALCSIZE](../vs140/CWnd--OnNcCalcSize.md), and [WM_GETMINMAXINFO](../vs140/CWnd--OnGetMinMaxInfo.md) messages to the combo box.  
  
 These messages are handled by default by the [OnNcCreate](../vs140/CWnd--OnNcCreate.md), [OnCreate](../vs140/CWnd--OnCreate.md), [OnNcCalcSize](../vs140/CWnd--OnNcCalcSize.md), and [OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md) member functions in the `CWnd` base class. To extend the default message handling, derive a class from `CComboBox`, add a message map to the new class, and override the preceding message-handler member functions. Override `OnCreate`, for example, to perform needed initialization for a new class.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to a combo-box control. :  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
-   **WS_VSCROLL** To add vertical scrolling for the list box in the combo box  
  
-   **WS_HSCROLL** To add horizontal scrolling for the list box in the combo box  
  
-   **WS_GROUP** To group controls  
  
-   **WS_TABSTOP** To include the combo box in the tabbing order  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#2)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::CComboBox](../vs140/CComboBox--CComboBox.md)   
 [Combo-Box Styles](../vs140/Combo-Box-Styles.md)