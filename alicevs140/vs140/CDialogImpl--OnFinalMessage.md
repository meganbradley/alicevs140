---
title: "CDialogImpl::OnFinalMessage"
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
ms.assetid: 1b16f4dc-80e5-4b11-a0ff-f224ffe2d774
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogImpl::OnFinalMessage
Called after receiving the last message (typically `WM_NCDESTROY`).  
  
## Syntax  
  
```  
  
      virtual void OnFinalMessage(  
   HWND hWnd   
);  
```  
  
#### Parameters  
 `hWnd`  
 [in] A handle to the window being destroyed.  
  
## Remarks  
 Note that if you want to automatically delete your object upon the window destruction, you can call `delete this;` here.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDialogImpl Class](../vs140/CDialogImpl-Class.md)   
 [CDialogImpl::GetDialogProc](../vs140/CDialogImpl--GetDialogProc.md)