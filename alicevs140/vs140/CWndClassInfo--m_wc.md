---
title: "CWndClassInfo::m_wc"
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
ms.assetid: 240a8e76-d789-4cfe-a97c-4d819483c33b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWndClassInfo::m_wc
Maintains the window class information in a [WNDCLASSEX](http://msdn.microsoft.com/library/windows/desktop/ms633577) structure.  
  
## Syntax  
  
```  
  
WNDCLASSEX m_wc;  
  
```  
  
## Remarks  
 If you have specified the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) (the default in [CWindowImpl](../vs140/CWindowImpl-Class.md)) or the [DECLARE_WND_CLASS_EX](../vs140/DECLARE_WND_CLASS_EX.md) macro, `m_wc` contains information about a new window class.  
  
 If you have specified the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro, `m_wc` contains information about a superclass — a window class that is based on an existing class but uses a different window procedure. [m_lpszOrigName](../vs140/CWndClassInfo--m_lpszOrigName.md) and [pWndProc](../vs140/CWndClassInfo--pWndProc.md) save the existing window class's name and window procedure, respectively.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWndClassInfo Class](../vs140/CWndClassInfo-Class.md)