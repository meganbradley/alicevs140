---
title: "CAtlServiceModuleT::RegisterAppId"
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
ms.assetid: acadc332-0621-47d2-af95-5ab6373e9ffe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::RegisterAppId
Registers the service in the registry.  
  
## Syntax  
  
```  
  
      inline HRESULT RegisterAppId(  
   bool bService = false   
) throw( );  
```  
  
#### Parameters  
 *bService*  
 Must be true to register as a service.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)