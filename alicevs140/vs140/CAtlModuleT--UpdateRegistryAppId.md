---
title: "CAtlModuleT::UpdateRegistryAppId"
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
ms.assetid: 2336c999-215e-42e0-bfe5-0bff638a5886
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModuleT::UpdateRegistryAppId
Updates the EXE information in the registry.  
  
## Syntax  
  
```  
  
      static HRESULT WINAPI UpdateRegistryAppId(  
   BOOL /*bRegister*/  
) throw( );  
```  
  
#### Parameters  
 `bRegister`  
 Reserved.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlModuleT Class](../vs140/CAtlModuleT-Class.md)