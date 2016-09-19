---
title: "CWnd::GetNextDlgTabItem"
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
ms.assetid: a693ad27-f55f-4a81-b612-8052dafaf260
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetNextDlgTabItem
Retrieves a pointer to the first control that was created with the [WS_TABSTOP](../vs140/Window-Styles.md) style and that precedes or follows the specified control.  
  
## Syntax  
  
```  
  
      CWnd* GetNextDlgTabItem(  
   CWnd* pWndCtl,  
   BOOL bPrevious = FALSE   
) const;  
COleControlSiteOrWnd* GetNextDlgTabItem(  
   COleControlSiteOrWnd *pCurSiteOrWnd,   
   BOOL bPrevious  
) const;  
```  
  
#### Parameters  
 `pWndCtl`  
 Identifies the control to be used as the starting point for the search.  
  
 `pCurSiteOrWnd`  
 Identifies the **COleControlSiteOrWnd** control. For more information about `COleControlSiteOrWnd`, see [CWnd::GetNextDlgGroupItem](../vs140/CWnd--GetNextDlgGroupItem.md).  
  
 `bPrevious`  
 Specifies how the function is to search the dialog box. If **TRUE**, the function searches for the previous control in the dialog box; if **FALSE**, it searches for the next control.  
  
## Return Value  
 Pointer to the previous or next control that has the **WS_TABSTOP** style, if the member function is successful.  
  
 The returned pointer may be temporary and should not be stored for later use.  
  
 For more information about `COleControlSiteOrWnd`, see [CWnd::GetNextDlgGroupItem](../vs140/CWnd--GetNextDlgGroupItem.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetNextDlgGroupItem](../vs140/CWnd--GetNextDlgGroupItem.md)   
 [GetNextDlgTabItem](http://msdn.microsoft.com/library/windows/desktop/ms645495)