---
title: "CContainedWindowT::RegisterWndSuperclass"
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
ms.assetid: a925a3f7-4f1b-4ed2-9ea7-3ccd67b66a44
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::RegisterWndSuperclass
Called by [Create](../vs140/CContainedWindowT--Create.md) to register the window class of the contained window.  
  
## Syntax  
  
```  
  
ATOM RegisterWndSuperClass( );  
  
```  
  
## Return Value  
 If successful, an atom that uniquely identifies the window class being registered; otherwise, zero.  
  
## Remarks  
 This window class is based on an existing class but uses [CContainedWindowT::WindowProc](../vs140/CContainedWindowT--WindowProc.md). The existing window class's name and window procedure are saved in [m_lpszClassName](../vs140/CContainedWindowT--m_lpszClassName.md) and [m_pfnSuperWindowProc](../vs140/CContainedWindowT--m_pfnSuperWindowProc.md), respectively.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::CContainedWindowT](../vs140/CContainedWindowT--CContainedWindowT.md)