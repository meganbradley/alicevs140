---
title: "CWnd::SendDlgItemMessage"
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
ms.assetid: b6f0c0da-2a12-4e25-b898-61d6d20fc03c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SendDlgItemMessage
Sends a message to a control.  
  
## Syntax  
  
```  
  
      LRESULT SendDlgItemMessage(  
   int nID,  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
);  
```  
  
#### Parameters  
 `nID`  
 Specifies the identifier of the dialog control that will receive the message.  
  
 `message`  
 Specifies the message to be sent.  
  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information.  
  
## Return Value  
 Specifies the value returned by the control's window procedure, or 0 if the control was not found.  
  
## Remarks  
 The `SendDlgItemMessage` member function does not return until the message has been processed.  
  
 Using `SendDlgItemMessage` is identical to obtaining a `CWnd`* to the given control and calling the [SendMessage](../vs140/CWnd--SendMessage.md) member function.  
  
## Example  
 [!CODE [NVC_MFCWindowing#113](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#113)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SendMessage](../vs140/CWnd--SendMessage.md)   
 [SendDlgItemMessage](http://msdn.microsoft.com/library/windows/desktop/ms645515)