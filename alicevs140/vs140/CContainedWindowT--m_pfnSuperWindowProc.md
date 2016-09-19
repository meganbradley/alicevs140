---
title: "CContainedWindowT::m_pfnSuperWindowProc"
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
ms.assetid: 12d97efd-e53e-4a6d-aa39-c288c8be63c7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::m_pfnSuperWindowProc
If the contained window is subclassed, `m_pfnSuperWindowProc` points to the original window procedure of the window class.  
  
## Syntax  
  
```  
  
WNDPROC m_pfnSuperWindowProc;  
  
```  
  
## Remarks  
 If the contained window is superclassed, meaning it is based on a window class that modifies an existing class, `m_pfnSuperWindowProc` points to the existing window class's window procedure.  
  
 The [DefWindowProc](../vs140/CContainedWindowT--DefWindowProc.md) method sends message information to the window procedure saved in `m_pfnSuperWindowProc`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::Create](../vs140/CContainedWindowT--Create.md)   
 [CContainedWindowT::SubclassWindow](../vs140/CContainedWindowT--SubclassWindow.md)