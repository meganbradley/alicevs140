---
title: "CWnd::OnGetDlgCode"
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
ms.assetid: 614afa07-f1a6-475a-b600-0883529c7c54
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnGetDlgCode
Called for a control so the control can process arrow-key and TAB-key input itself.  
  
## Syntax  
  
```  
  
afx_msg UINT OnGetDlgCode( );  
```  
  
## Return Value  
 One or more of the following values, indicating which type of input the application processes:  
  
-   **DLGC_BUTTON** Button (generic).  
  
-   **DLGC_DEFPUSHBUTTON** Default pushbutton.  
  
-   **DLGC_HASSETSEL EM_SETSEL** messages.  
  
-   **DLGC_UNDEFPUSHBUTTON** No default pushbutton processing. (An application can use this flag with **DLGC_BUTTON** to indicate that it processes button input but relies on the system for default pushbutton processing.)  
  
-   **DLGC_RADIOBUTTON** Radio button.  
  
-   **DLGC_STATIC** Static control.  
  
-   **DLGC_WANTALLKEYS** All keyboard input.  
  
-   **DLGC_WANTARROWS** Arrow keys.  
  
-   **DLGC_WANTCHARS** `WM_CHAR` messages.  
  
-   **DLGC_WANTMESSAGE** All keyboard input. The application passes this message on to the control.  
  
-   **DLGC_WANTTAB** TAB key.  
  
## Remarks  
 Normally, Windows handles all arrow-key and TAB-key input to a `CWnd` control. By overriding `OnGetDlgCode`, a `CWnd` control can choose a particular type of input to process itself.  
  
 The default `OnGetDlgCode` functions for the predefined control classes return a code appropriate for each class.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_GETDLGCODE](http://msdn.microsoft.com/library/windows/desktop/ms645425)