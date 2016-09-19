---
title: "AtlComModuleRevokeClassObjects"
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
ms.assetid: 317994ca-d281-47cd-9430-d138b714a04a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlComModuleRevokeClassObjects
This function is called to remove the class factory/factories from the Running Object Table.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLINLINE ATLAPI AtlComModuleRevokeClassObjects(  
_ATL_COM_MODULE * pComModule   
);  
```  
  
#### Parameters  
 `pComModule`  
 Pointer to the COM module.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This helper function is utilized by [CComModule::RevokeClassObjects](../vs140/CComModule--RevokeClassObjects.md) (obsolete in ATL 7.0) and [CAtlExeModuleT::RevokeClassObjects](../vs140/CAtlExeModuleT--RevokeClassObjects.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Server Registration Global Functions](../vs140/Server-Registration-Global-Functions.md)