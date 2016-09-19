---
title: "CAtlDllModuleT::DllUnregisterServer"
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
ms.assetid: d89a0253-f2a1-40d9-83e7-9ec0cb0682cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlDllModuleT::DllUnregisterServer
Removes entries in the system registry for objects in the DLL.  
  
## Syntax  
  
```  
  
      HRESULT DllUnregisterServer(  
   BOOL bUnRegTypeLib = TRUE   
) throw( );  
```  
  
#### Parameters  
 `bUnRegTypeLib`  
 TRUE if the type library is to be removed from the registry. The default value is TRUE.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlDllModuleT Class](../vs140/CAtlDllModuleT-Class.md)   
 [CAtlDllModuleT::DllRegisterServer](../vs140/CAtlDllModuleT--DllRegisterServer.md)