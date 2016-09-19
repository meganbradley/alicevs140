---
title: "CWnd::OnNotify"
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
ms.assetid: fb4687ed-4198-4e7c-9ace-caf87d1e7cb6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnNotify
The framework calls this member function to inform the parent window of a control that an event has occurred in the control or that the control requires some kind of information.  
  
## Syntax  
  
```  
  
      virtual BOOL OnNotify(   
   WPARAM wParam,   
   LPARAM lParam,   
   LRESULT* pResult    
);  
```  
  
#### Parameters  
 `wParam`  
 Identifies the control that sends the message if the message is from a control. Otherwise, `wParam` is 0.  
  
 `lParam`  
 Pointer to a notification message (**NMHDR**) structure that contains the notification code and additional information. For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.  
  
 `pResult`  
 Pointer to an **LRESULT** variable in which to store the result code if the message is handled.  
  
## Return Value  
 An application returns nonzero if it processes this message; otherwise 0.  
  
## Remarks  
 `OnNotify` processes the message map for control notification.  
  
 Override this member function in your derived class to handle the **WM_NOTIFY** message. An override will not process the message map unless the base class `OnNotify` is called.  
  
 For more information on the WM_NOTIFY message, see Technical Note 61 (TN061), [ON_NOTIFY and WM_NOTIFY messages](../vs140/TN061--ON_NOTIFY-and-WM_NOTIFY-Messages.md). You may also be interested the related topics described in [Control Topics](../vs140/Controls--MFC-.md), and TN062, [Message Reflection for Windows Controls](../vs140/TN062--Message-Reflection-for-Windows-Controls.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)