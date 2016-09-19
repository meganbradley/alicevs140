---
title: "AtlUnRegisterTypeLib"
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
ms.assetid: 962b0fc8-e423-4341-a0f4-22c93760926a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlUnRegisterTypeLib
This function is called to unregister a type library.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLAPI AtlUnRegisterTypeLib(  
HINSTANCE hInstTypeLib,  
LPCOLESTR lpszIndex   
);  
```  
  
#### Parameters  
 `hInstTypeLib`  
 The handle to the module instance.  
  
 `lpszIndex`  
 String in the format "\\\N", where N is the integer index of the type library resource. Can be NULL if no index is required.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This helper function is utilized by [CAtlComModule::UnRegisterTypeLib](../vs140/CAtlComModule--UnRegisterTypeLib.md) and [AtlComModuleUnregisterServer](../vs140/AtlComModuleUnregisterServer.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Server Registration Global Functions](../vs140/Server-Registration-Global-Functions.md)   
 [AtlRegisterTypeLib](../vs140/AtlRegisterTypeLib.md)   
 [AtlLoadTypeLib](../vs140/AtlLoadTypeLib.md)