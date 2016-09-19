---
title: "AtlComModuleGetClassObject"
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
ms.assetid: 08b825de-a295-4eae-b726-cbd1de9a6670
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlComModuleGetClassObject
This function is called to return the class factory.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLINLINE ATLAPI AtlComModuleGetClassObject(  
_ATL_COM_MODULE * pComModule,  
REFCLSID rclsid,  
REFIID riid,  
LPVOID* ppv   
);  
```  
  
#### Parameters  
 `pComModule`  
 Pointer to the COM module.  
  
 `rclsid`  
 The CLSID of the object to be created.  
  
 `riid`  
 The IID of the requested interface.  
  
 `ppv`  
 A pointer to the interface pointer identified by `riid`. If the object does not support this interface, `ppv` is set to NULL.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This helper function is utilized by [CComModule::GetClassObject](../vs140/CComModule--GetClassObject.md) (obsolete in ATL 7.0) and [CAtlDllModuleT::GetClassObject](../vs140/CAtlDllModuleT--GetClassObject.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Server Registration Global Functions](../vs140/Server-Registration-Global-Functions.md)