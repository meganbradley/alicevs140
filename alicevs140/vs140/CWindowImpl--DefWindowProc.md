---
title: "CWindowImpl::DefWindowProc"
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
ms.assetid: 64df2bb7-5f58-4218-a168-a28b553e763f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::DefWindowProc
Called by [WindowProc](../vs140/CWindowImpl--WindowProc.md) to process messages not handled by the message map.  
  
## Syntax  
  
```  
  
      LRESULT DefWindowProc(  
   UINT uMsg,  
   WPARAM wParam,  
   LPARAM lParam   
);  
LRESULT DefWindowProc( );  
```  
  
#### Parameters  
 `uMsg`  
 [in] The message sent to the window.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
## Return Value  
 The result of the message processing.  
  
## Remarks  
 By default, `DefWindowProc` calls the [CallWindowProc](http://msdn.microsoft.com/library/windows/desktop/ms633571) Win32 function to send the message information to the window procedure specified in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md).  
  
 The function with no parameters automatically retrieves the needed parameters from the current message.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)