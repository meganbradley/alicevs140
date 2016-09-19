---
title: "CComModule::GetResourceInstance"
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
ms.assetid: 7df0ac23-94fd-47bc-b8b2-9961cd6d0be6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::GetResourceInstance
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
HINSTANCE GetResourceInstance( ) throw( );  
  
```  
  
## Return Value  
 An `HINSTANCE`.  
  
## Remarks  
 Returns the [m_hInstResource](../vs140/CComModule--m_hInstResource.md) data member.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::GetModuleInstance](../vs140/CComModule--GetModuleInstance.md)   
 [CComModule::GetTypeLibInstance](../vs140/CComModule--GetTypeLibInstance.md)