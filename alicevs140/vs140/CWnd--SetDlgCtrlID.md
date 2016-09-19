---
title: "CWnd::SetDlgCtrlID"
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
ms.assetid: 3832a584-e88d-458c-96dc-d95e3a5a5c13
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetDlgCtrlID
Sets the window ID or control ID for the window to a new value.  
  
## Syntax  
  
```  
  
      int SetDlgCtrlID(  
   int nID   
);  
```  
  
#### Parameters  
 `nID`  
 The new value to set for the control's identifier.  
  
## Return Value  
 The previous identifier of the window, if successful; otherwise 0.  
  
## Remarks  
 The window can be any child window, not only a control in a dialog box. The window cannot be a top-level window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDlgCtrlID](../vs140/CWnd--GetDlgCtrlID.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWnd::CreateEx](../vs140/CWnd--CreateEx.md)   
 [CWnd::GetDlgItem](../vs140/CWnd--GetDlgItem.md)