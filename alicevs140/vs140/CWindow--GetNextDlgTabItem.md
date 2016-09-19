---
title: "CWindow::GetNextDlgTabItem"
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
ms.assetid: 43e4774f-d8bc-4251-b36a-b28eb49023e7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetNextDlgTabItem
Retrieves the previous or next control having the **WS_TABSTOP** style.  
  
## Syntax  
  
```  
  
      HWND GetNextDlgTabItem(  
   HWND hWndCtl,  
   BOOL bPrevious = FALSE   
) const throw();  
```  
  
## Remarks  
 See [GetNextDlgTabItem](http://msdn.microsoft.com/library/windows/desktop/ms645495) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetNextDlgGroupItem](../vs140/CWindow--GetNextDlgGroupItem.md)