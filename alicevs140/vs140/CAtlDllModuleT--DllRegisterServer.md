---
title: "CAtlDllModuleT::DllRegisterServer"
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
ms.assetid: ccce6d40-7739-4352-a1e7-e494ca65d62e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlDllModuleT::DllRegisterServer
Adds entries to the system registry for objects in the DLL.  
  
## Syntax  
  
```  
  
      HRESULT DllRegisterServer(  
   BOOL bRegTypeLib = TRUE   
) throw( );  
```  
  
#### Parameters  
 `bRegTypeLib`  
 TRUE if the type library is to be registered. The default value is TRUE.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlDllModuleT Class](../vs140/CAtlDllModuleT-Class.md)   
 [CAtlDllModuleT::DllUnregisterServer](../vs140/CAtlDllModuleT--DllUnregisterServer.md)