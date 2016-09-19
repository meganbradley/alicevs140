---
title: "CWndClassInfo::m_lpszCursorID"
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
ms.assetid: 22e3f93c-76e7-4d2d-a291-aab465727435
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWndClassInfo::m_lpszCursorID
Specifies either the name of the cursor resource or the resource identifier in the low-order word and zero in the high-order word.  
  
## Syntax  
  
```  
  
LPCTSTR m_lpszCursorID;  
  
```  
  
## Remarks  
 When the window class is registered, the handle to the cursor identified by `m_lpszCursorID` is retrieved and stored by [m_wc](../vs140/CWndClassInfo--m_wc.md).  
  
 `CWndClassInfo` uses `m_lpszCursorID` only when the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) (the default in [CWindowImpl](../vs140/CWindowImpl-Class.md)) or the [DECLARE_WND_CLASS_EX](../vs140/DECLARE_WND_CLASS_EX.md) macro is specified. In this case, `m_lpszCursorID` is initialized to **IDC_ARROW**. For more information, see the [CWndClassInfo](../vs140/CWndClassInfo-Class.md) overview.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWndClassInfo Class](../vs140/CWndClassInfo-Class.md)   
 [CWndClassInfo::m_bSystemCursor](../vs140/CWndClassInfo--m_bSystemCursor.md)