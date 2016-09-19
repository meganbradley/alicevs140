---
title: "CRichEditCtrl::Create"
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
ms.assetid: 3546c313-6d8d-4716-9708-ce82d1e4e563
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditCtrl::Create
Creates the Windows rich edit control and associates it with this `CRichEditCtrl` object.  
  
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
 Specifies the edit control's style. Apply a combination of the window styles listed in the **Remarks** section below, and [edit control styles](http://msdn.microsoft.com/library/windows/desktop/bb775464), described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `rect`  
 Specifies the edit control's size and position. Can be a [CRect](../vs140/CRect-Class.md) object or [RECT](../vs140/RECT-Structure.md) structure.  
  
 `pParentWnd`  
 Specifies the edit control's parent window (often a [CDialog](../vs140/CDialog-Class.md)). It must not be **NULL**.  
  
 `nID`  
 Specifies the edit control's ID.  
  
## Return Value  
 Nonzero if initialization is successful; otherwise, 0.  
  
## Remarks  
 You construct a `CRichEditCtrl` object in two steps. First, call the [CRichEditCtrl](../vs140/CRichEditCtrl--CRichEditCtrl.md) constructor, then call **Create**, which creates the Windows edit control and attaches it to the `CRichEditCtrl` object.  
  
 When you create a rich edit control with this function, first you must load the necessary common controls library. To load the libary, call the global function [AfxInitRichEdit](../vs140/AfxInitRichEdit.md), which in turn initializes the common controls library. You need to call `AfxInitRichEdit` only once in your process.  
  
 When **Create** executes, Windows sends the [WM_NCCREATE](../vs140/CWnd--OnNcCreate.md), [WM_NCCALCSIZE](../vs140/CWnd--OnNcCalcSize.md), [WM_CREATE](../vs140/CWnd--OnCreate.md), and [WM_GETMINMAXINFO](../vs140/CWnd--OnGetMinMaxInfo.md) messages to the edit control.  
  
 These messages are handled by default by the [OnNcCreate](../vs140/CWnd--OnNcCreate.md), [OnNcCalcSize](../vs140/CWnd--OnNcCalcSize.md), [OnCreate](../vs140/CWnd--OnCreate.md), and [OnGetMinMaxInfo](../vs140/CWnd--OnGetMinMaxInfo.md) member functions in the `CWnd` base class. To extend the default message handling, derive a class from `CRichEditCtrl`, add a message map to the new class, and override the above message-handler member functions. Override `OnCreate`, for example, to perform needed initialization for the new class.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to an edit control.  
  
-   **WS_CHILD** Always.  
  
-   **WS_VISIBLE** Usually.  
  
-   **WS_DISABLED** Rarely.  
  
-   **WS_GROUP** To group controls.  
  
-   **WS_TABSTOP** To include edit control in the tabbing order.  
  
 For more information about window styles, see [CreateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632679) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CRichEditCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CRichEditCtrl#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CRichEditCtrl Class](../vs140/CRichEditCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::CreateEx](../vs140/CRichEditCtrl--CreateEx.md)   
 [CRichEditCtrl::CRichEditCtrl](../vs140/CRichEditCtrl--CRichEditCtrl.md)