---
title: "CComModule::m_hInstResource"
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
ms.assetid: 3128f561-c5e7-4cf0-a958-c76fa807149e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::m_hInstResource
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
HINSTANCE m_hInstResource;  
  
```  
  
## Remarks  
 By default, contains the handle to the module instance.  
  
 The [Init](../vs140/CComModule--Init.md) method sets `m_hInstResource` to the handle passed to **DLLMain** or `WinMain`. You can explicitly set `m_hInstResource` to the handle to a resource.  
  
 The [GetResourceInstance](../vs140/CComModule--GetResourceInstance.md) method returns the handle stored in `m_hInstResource`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)