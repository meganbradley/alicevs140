---
title: "CWndClassInfo::m_bSystemCursor"
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
ms.assetid: 86b9b3be-639a-490b-b83a-9afffb8715dc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWndClassInfo::m_bSystemCursor
If **TRUE**, the system cursor resource will be loaded when the window class is registered.  
  
## Syntax  
  
```  
  
BOOL m_bSystemCursor;  
  
```  
  
## Remarks  
 Otherwise, the cursor resource contained in your module will be loaded.  
  
 `CWndClassInfo` uses `m_bSystemCursor` only when the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) (the default in [CWindowImpl](../vs140/CWindowImpl-Class.md)) or the [DECLARE_WND_CLASS_EX](../vs140/DECLARE_WND_CLASS_EX.md) macro is specified. In this case, `m_bSystemCursor` is initialized to **TRUE**. For more information, see the [CWndClassInfo](../vs140/CWndClassInfo-Class.md) overview.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWndClassInfo Class](../vs140/CWndClassInfo-Class.md)   
 [CWndClassInfo::m_lpszCursorID](../vs140/CWndClassInfo--m_lpszCursorID.md)