---
title: "CMFCToolBarButton::NotifyCommand"
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
ms.assetid: 45bd674e-1e83-48aa-a299-ab26c9ba2825
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::NotifyCommand
Specifies whether the button processes the [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) message.  
  
## Syntax  
  
```  
virtual BOOL NotifyCommand(  
   int iNotifyCode  
);  
```  
  
#### Parameters  
 [in] `iNotifyCode`  
 The notification message that is associated with the command.  
  
## Return Value  
 This method returns `FALSE`.  
  
## Remarks  
 The framework calls this method when it is about to send a [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) message to the parent window.  
  
 By default, this method returns `FALSE`. Override this method to return `TRUE` if you want to process the `WM_COMMAND` message or `FALSE` to indicate that the parent toolbar should handle the message.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591)