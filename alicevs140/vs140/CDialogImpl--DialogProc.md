---
title: "CDialogImpl::DialogProc"
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
ms.assetid: 828fa7fc-dd61-4f72-954c-2185d17823fc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogImpl::DialogProc
This static function implements the dialog box procedure.  
  
## Syntax  
  
```  
  
      static LRESULT CALLBACK DialogProc(  
   HWND hWnd,  
   UINT uMsg,  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `hWnd`  
 [in] The handle to the dialog box.  
  
 `uMsg`  
 [in] The message sent to the dialog box.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
## Return Value  
 **TRUE** if the message is processed; otherwise, **FALSE**.  
  
## Remarks  
 `DialogProc` uses the default message map to direct messages to the appropriate handlers.  
  
 You can override `DialogProc` to provide a different mechanism for handling messages.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDialogImpl Class](../vs140/CDialogImpl-Class.md)   
 [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)