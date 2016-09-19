---
title: "CWindow::GotoDlgCtrl"
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
ms.assetid: af585bfa-6836-4889-b0a9-13b3c3513609
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GotoDlgCtrl
Sets the keyboard focus to a control in the dialog box.  
  
## Syntax  
  
```  
  
      void GotoDlgCtrl(  
   HWND hWndCtrl   
) const throw();  
```  
  
## Remarks  
 See [WM_NEXTDLGCTL](http://msdn.microsoft.com/library/windows/desktop/ms645432) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::NextDlgCtrl](../vs140/CWindow--NextDlgCtrl.md)   
 [CWindow::PrevDlgCtrl](../vs140/CWindow--PrevDlgCtrl.md)