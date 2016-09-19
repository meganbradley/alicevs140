---
title: "CWindow::GetNextDlgGroupItem"
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
ms.assetid: 530b4cdb-46de-436e-94d1-2b2fd57da289
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetNextDlgGroupItem
Retrieves the previous or next control within a group of controls.  
  
## Syntax  
  
```  
  
      HWND GetNextDlgGroupItem(  
   HWND hWndCtl,  
   BOOL bPrevious = FALSE   
) const throw();  
```  
  
## Remarks  
 See [GetNextDlgGroupItem](http://msdn.microsoft.com/library/windows/desktop/ms645492) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetNextDlgTabItem](../vs140/CWindow--GetNextDlgTabItem.md)