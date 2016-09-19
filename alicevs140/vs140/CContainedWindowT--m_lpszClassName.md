---
title: "CContainedWindowT::m_lpszClassName"
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
ms.assetid: 7c28191b-076a-4a24-909a-85f4b398646d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::m_lpszClassName
Specifies the name of an existing window class.  
  
## Syntax  
  
```  
  
LPTSTR m_lpszClassName;  
  
```  
  
## Remarks  
 When you create a window, [Create](../vs140/CContainedWindowT--Create.md) registers a new window class that is based on this existing class but uses [CContainedWindowT::WindowProc](../vs140/CContainedWindowT--WindowProc.md).  
  
 `m_lpszClassName` is initialized by the constructor. For an example, see the [CContainedWindowT](../vs140/CContainedWindowT-Class.md) overview.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)