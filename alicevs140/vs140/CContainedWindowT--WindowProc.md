---
title: "CContainedWindowT::WindowProc"
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
ms.assetid: 9e9435b2-f767-4d73-be2b-92b7e4334640
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::WindowProc
This static method implements the window procedure.  
  
## Syntax  
  
```  
  
      static LRESULT CALLBACK WindowProc(  
   HWND hWnd,  
   UINT uMsg,  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `hWnd`  
 [in] The handle to the window.  
  
 `uMsg`  
 [in] The message sent to the window.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
## Return Value  
 The result of the message processing.  
  
## Remarks  
 `WindowProc` directs messages to the message map identified by [m_dwMsgMapID](../vs140/CContainedWindowT--m_dwMsgMapID.md). If necessary, `WindowProc` calls [DefWindowProc](../vs140/CContainedWindowT--DefWindowProc.md) for additional message processing.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)   
 [ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md)