---
title: "CDialogImpl::StartDialogProc"
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
ms.assetid: 96d34eb1-a693-44e6-b048-5b95a3041a94
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogImpl::StartDialogProc
Called only once, when the first message is received, to process messages sent to the dialog box.  
  
## Syntax  
  
```  
  
      static LRESULT CALLBACK StartDialogProc(  
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
 The window procedure.  
  
## Remarks  
 After the initial call to `StartDialogProc`, `DialogProc` is set as a dialog procedure, and further calls go there.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDialogImpl Class](../vs140/CDialogImpl-Class.md)   
 [CDialogImpl::DialogProc](../vs140/CDialogImpl--DialogProc.md)