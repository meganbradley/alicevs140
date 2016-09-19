---
title: "CComModule::m_hInstTypeLib"
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
ms.assetid: 5fb6db16-1996-4f3c-a3ab-6fe782b1917f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::m_hInstTypeLib
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
HINSTANCE m_hInstTypeLib;  
  
```  
  
## Remarks  
 By default, contains the handle to the module instance.  
  
 The [Init](../vs140/CComModule--Init.md) method sets `m_hInstTypeLib` to the handle passed to **DLLMain** or `WinMain`. You can explicitly set `m_hInstTypeLib` to the handle to a type library.  
  
 The [GetTypeLibInstance](../vs140/CComModule--GetTypeLibInstance.md) method returns the handle stored in `m_hInstTypeLib`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)