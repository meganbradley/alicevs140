---
title: "CDialog::NextDlgCtrl"
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
ms.assetid: 58a0959c-f112-4d01-9ca0-66a947637b26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::NextDlgCtrl
Moves the focus to the next control in the dialog box.  
  
## Syntax  
  
```  
  
void NextDlgCtrl( ) const;  
```  
  
## Remarks  
 If the focus is at the last control in the dialog box, it moves to the first control.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::PrevDlgCtrl](../vs140/CDialog--PrevDlgCtrl.md)   
 [CDialog::GotoDlgCtrl](../vs140/CDialog--GotoDlgCtrl.md)