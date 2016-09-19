---
title: "CWndClassInfo::m_szAutoName"
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
ms.assetid: 1689fdd0-bebb-483e-a3d5-4ce0ad7aa245
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWndClassInfo::m_szAutoName
Holds the name of the window class.  
  
## Syntax  
  
```  
  
TCHAR m_szAutoName[13];  
  
```  
  
## Remarks  
 `CWndClassInfo` uses `m_szAutoName` only if **NULL** is passed for the `WndClassName` parameter to [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md), the [DECLARE_WND_CLASS_EX](../vs140/DECLARE_WND_CLASS_EX.md) or [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md). ATL will construct a name when the window class is registered.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWndClassInfo Class](../vs140/CWndClassInfo-Class.md)