---
title: "CWindow::SendDlgItemMessage"
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
ms.assetid: df70e8ab-2103-49a4-8bb1-3bc43b12b7d5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SendDlgItemMessage
Sends a message to a control.  
  
## Syntax  
  
```  
  
      LRESULT SendDlgItemMessage(  
   int nID,  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
) throw();  
```  
  
## Remarks  
 See [SendDlgItemMessage](http://msdn.microsoft.com/library/windows/desktop/ms645515) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SendMessage](../vs140/CWindow--SendMessage.md)