---
title: "CWnd::DefWindowProc"
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
ms.assetid: 4a8b4438-2dad-48d6-bb22-9685f2902c58
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::DefWindowProc
Calls the default window procedure, which provides default processing for any window message that an application does not process.  
  
## Syntax  
  
```  
  
      virtual LRESULT DefWindowProc(  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `message`  
 Specifies the Windows message to be processed.  
  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information.  
  
## Return Value  
 Depends on the message sent.  
  
## Remarks  
 This member function ensures that every message is processed. It should be called with the same parameters as those received by the window procedure.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Default](../vs140/CWnd--Default.md)   
 [DefWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633572)