---
title: "CWindowImpl::OnFinalMessage"
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
ms.assetid: 0e964fb3-cee1-4c7b-b3da-51f9645a390d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::OnFinalMessage
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
 The default implementation of `OnFinalMessage` does nothing, but you can override this function to handle cleanup before destroying a window. If you want to automatically delete your object upon the window destruction, you can call `delete this;` in this function.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)   
 [CWindowImpl::GetWindowProc](../vs140/CWindowImpl--GetWindowProc.md)   
 [CWindowImpl::UnsubclassWindow](../vs140/CWindowImpl--UnsubclassWindow.md)