---
title: "CMFCToolBarDateTimeCtrl::NotifyCommand"
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
ms.assetid: 15b78303-d70b-4a85-8e7d-cf9af1f4a66b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::NotifyCommand
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
 `TRUE` if the button processes the `WM_COMMAND` message, or `FALSE` to indicate that the message should be handled by the parent toolbar.  
  
## Remarks  
 The framework calls this method when it is about to send a [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) message to the parent window.  
  
 This method extends the base class implementation ([CMFCToolBarButton::NotifyCommand](../vs140/CMFCToolBarButton--NotifyCommand.md)) by processing the [DTN_DATETIMECHANGE](http://msdn.microsoft.com/library/windows/desktop/bb761737) notification. It updates the internal time status and updates the time property of all `CMFCToolBarDateTimeCtrl` objects with the same command ID.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591)   
 [CMFCToolBarButton::NotifyCommand](../vs140/CMFCToolBarButton--NotifyCommand.md)   
 [DTN_DATETIMECHANGE](http://msdn.microsoft.com/library/windows/desktop/bb761737)