---
title: "CAtlModuleT::UnregisterAppId"
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
ms.assetid: 2d29fd1b-6991-481c-922e-f64c095cfd1b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModuleT::UnregisterAppId
Removes the EXE from the registry.  
  
## Syntax  
  
```  
  
HRESULT UnregisterAppId( ) throw( );  
  
```  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlModuleT Class](../vs140/CAtlModuleT-Class.md)   
 [CAtlModuleT::RegisterAppId](../vs140/CAtlModuleT--RegisterAppId.md)