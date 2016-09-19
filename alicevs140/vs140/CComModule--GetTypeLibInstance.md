---
title: "CComModule::GetTypeLibInstance"
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
ms.assetid: 09f0bbc4-908b-4536-aa77-7b9a1c7183fb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::GetTypeLibInstance
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
HINSTANCE GetTypeLibInstance( ) const throw( );  
  
```  
  
## Return Value  
 An `HINSTANCE`.  
  
## Remarks  
 Returns the [m_hInstTypeLib](../vs140/CComModule--m_hInstTypeLib.md) data member.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::GetModuleInstance](../vs140/CComModule--GetModuleInstance.md)   
 [CComModule::GetResourceInstance](../vs140/CComModule--GetResourceInstance.md)