---
title: "AtlRegisterTypeLib"
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
ms.assetid: aaf0007a-0ac8-4541-9cd3-1a26a5727a40
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlRegisterTypeLib
This function is called to register a type library.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLAPI AtlRegisterTypeLib(  
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
 This helper function is utilized by [AtlComModuleUnregisterServer](../vs140/AtlComModuleUnregisterServer.md) and [CAtlComModule::RegisterTypeLib](../vs140/CAtlComModule--RegisterTypeLib.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Server Registration Global Functions](../vs140/Server-Registration-Global-Functions.md)   
 [AtlLoadTypeLib](../vs140/AtlLoadTypeLib.md)   
 [AtlUnRegisterTypeLib](../vs140/AtlUnRegisterTypeLib.md)