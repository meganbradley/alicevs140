---
title: "CDialog::PrevDlgCtrl"
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
ms.assetid: 5892530b-9cd1-4f6f-b0b0-b4c37e1d62c3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::PrevDlgCtrl
Sets the focus to the previous control in the dialog box.  
  
## Syntax  
  
```  
  
void PrevDlgCtrl( ) const;  
```  
  
## Remarks  
 If the focus is at the first control in the dialog box, it moves to the last control in the box.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::NextDlgCtrl](../vs140/CDialog--NextDlgCtrl.md)   
 [CDialog::GotoDlgCtrl](../vs140/CDialog--GotoDlgCtrl.md)