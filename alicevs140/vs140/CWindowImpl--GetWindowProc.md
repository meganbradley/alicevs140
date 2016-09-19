---
title: "CWindowImpl::GetWindowProc"
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
ms.assetid: 006421b0-30ec-4e02-ad5c-b0a3890c2c3b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::GetWindowProc
Returns `WindowProc`, the current window procedure.  
  
## Syntax  
  
```  
  
virtual WNDPROC GetWindowProc( );  
  
```  
  
## Return Value  
 The current window procedure.  
  
## Remarks  
 Override this method to replace the window procedure with your own.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)   
 [CWindowImpl::OnFinalMessage](../vs140/CWindowImpl--OnFinalMessage.md)   
 [CWindowImpl::UnsubclassWindow](../vs140/CWindowImpl--UnsubclassWindow.md)   
 [CWindowImpl::WindowProc](../vs140/CWindowImpl--WindowProc.md)