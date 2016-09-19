---
title: "CWindowImpl::UnsubclassWindow"
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
ms.assetid: 907e8421-c242-4a1e-9c4d-206f6eb5793b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindowImpl::UnsubclassWindow
Detaches the subclassed window from the `CWindowImpl` object and restores the original window procedure, saved in [m_pfnSuperWindowProc](../vs140/CWindowImpl--m_pfnSuperWindowProc.md).  
  
## Syntax  
  
```  
  
HWND UnsubclassWindow( );  
  
```  
  
## Return Value  
 The handle to the window previously subclassed.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindowImpl Class](../vs140/CWindowImpl-Class.md)   
 [CWindowImpl::SubclassWindow](../vs140/CWindowImpl--SubclassWindow.md)