---
title: "CComModule::GetModuleInstance"
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
ms.assetid: 5c845573-4eab-44aa-81f2-4183e9e19431
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::GetModuleInstance
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
HINSTANCE GetModuleInstance( ) throw( );  
  
```  
  
## Return Value  
 The `HINSTANCE` identifying this module.  
  
## Remarks  
 Returns the [m_hInst](../vs140/CComModule--m_hInst.md) data member.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::GetResourceInstance](../vs140/CComModule--GetResourceInstance.md)   
 [CComModule::GetTypeLibInstance](../vs140/CComModule--GetTypeLibInstance.md)