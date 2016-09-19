---
title: "CDialog::GotoDlgCtrl"
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
ms.assetid: 171bc5b7-5ecb-4bec-a0b5-5b56c5ebbddd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::GotoDlgCtrl
Moves the focus to the specified control in the dialog box.  
  
## Syntax  
  
```  
  
      void GotoDlgCtrl(  
   CWnd* pWndCtrl  
);  
```  
  
#### Parameters  
 `pWndCtrl`  
 Identifies the window (control) that is to receive the focus.  
  
## Remarks  
 To get a pointer to the control (child window) to pass as `pWndCtrl`, call the `CWnd::GetDlgItem` member function, which returns a pointer to a [CWnd](../vs140/CWnd-Class.md) object.  
  
## Example  
 See the example for [CWnd::GetDlgItem](../vs140/CWnd--GetDlgItem.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDlgItem](../vs140/CWnd--GetDlgItem.md)   
 [CDialog::PrevDlgCtrl](../vs140/CDialog--PrevDlgCtrl.md)   
 [CDialog::NextDlgCtrl](../vs140/CDialog--NextDlgCtrl.md)