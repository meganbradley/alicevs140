---
title: "CAtlComModule::UnregisterServer"
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
ms.assetid: 37808de3-3f24-48e6-97c9-e26c3c9cda74
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlComModule::UnregisterServer
Call this method to unregister each object in the object map.  
  
## Syntax  
  
```  
  
      HRESULT UnregisterServer(  
   BOOL bRegTypeLib = FALSE,  
   const CLSID* pCLSID = NULL   
);  
```  
  
#### Parameters  
 `bRegTypeLib`  
 TRUE if the type library is to be unregistered. The default value is FALSE.  
  
 `pCLSID`  
 Points to the CLSID of the object to be unregistered. If NULL (the default value), all objects in the object map will be unregistered.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Calls the global function [AtlComModuleUnregisterServer](../vs140/AtlComModuleUnregisterServer.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlComModule Class](../vs140/CAtlComModule-Class.md)   
 [CAtlComModule::RegisterServer](../vs140/CAtlComModule--RegisterServer.md)