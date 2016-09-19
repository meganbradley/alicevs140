---
title: "CWndClassInfo::m_lpszOrigName"
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
ms.assetid: af070001-4305-4914-9166-1bb6a711575c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWndClassInfo::m_lpszOrigName
Contains the name of an existing window class.  
  
## Syntax  
  
```  
  
LPCTSTR m_lpszOrigName;  
  
```  
  
## Remarks  
 `CWndClassInfo` uses `m_lpszOrigName` only when you include the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro in your class definition. In this case, `CWndClassInfo` registers a window class based on the class named by `m_lpszOrigName`. For more information, see the [CWndClassInfo](../vs140/CWndClassInfo-Class.md) overview.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWndClassInfo Class](../vs140/CWndClassInfo-Class.md)   
 [CWndClassInfo::m_wc](../vs140/CWndClassInfo--m_wc.md)   
 [CWndClassInfo::pWndProc](../vs140/CWndClassInfo--pWndProc.md)