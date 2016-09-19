---
title: "CWnd::OnChangeUIState"
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
ms.assetid: 0de6ae0a-7f4b-417a-9591-5ea4e74817d0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnChangeUIState
Called when the user interface (UI) state should be changed.  
  
## Syntax  
  
```  
  
      afx_msg void OnChangeUIState(  
   UINT nAction,  
   UINT nUIElement  
);  
```  
  
#### Parameters  
 `nAction`  
 Specifies the action to be taken. Can be one of the following values:  
  
-   **UIS_CLEAR** The UI state element (specified by `nUIElement`) should be hidden.  
  
-   **UIS_INITIALIZE** The UI state element (specified by `nUIElement`) should be changed based on the last input event. For more information, see the **Remarks** section of [WM_CHANGEUISTATE](http://msdn.microsoft.com/library/windows/desktop/ms646342).  
  
-   **UIS_SET** The UI state element (specified by `nUIElement`) should be visible.  
  
 `nUIElement`  
 Specifies which UI state elements are affected or the style of the control. Can be one of the following values:  
  
-   **UISF_HIDEACCEL** Keyboard accelerators.  
  
-   **UISF_HIDEFOCUS** Focus indicators.  
  
-   **UISF_ACTIVE Windows XP:** A control should be drawn in the style used for active controls.  
  
## Remarks  
 This member function emulates the functionality of the [WM_CHANGEUISTATE](http://msdn.microsoft.com/library/windows/desktop/ms646342) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnQueryUIState](../vs140/CWnd--OnQueryUIState.md)   
 [CWnd::OnUpdateUIState](../vs140/CWnd--OnUpdateUIState.md)