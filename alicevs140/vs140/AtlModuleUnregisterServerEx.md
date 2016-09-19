---
title: "AtlModuleUnregisterServerEx"
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
ms.assetid: 15c611ba-9fbe-4b1f-b041-9676911ad4ab
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlModuleUnregisterServerEx
Unregisters every object in the object map.  
  
 **Note** This function is obsolete in Visual C++ .NET 2002 and later but is available for backward compatibility with projects created with previous versions of Visual C++.  
  
## Syntax  
  
```  
  
      ATLAPI AtlModuleUnregisterServerEx(  
   _ATL_MODULE* pM,  
   BOOL bUnRegTypeLib,  
   const CLSID* pCLSID   
);  
```  
  
#### Parameters  
 `pM`  
 Pointer to a `CComModule` class or derived class.  
  
 `bUnRegTypeLib`  
 TRUE if the type library is to be registered.  
  
 `pCLSID`  
 Points to the CLSID of the object to be unregistered. If NULL, all objects in the object map will be unregistered.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This function walks the ATL object map and unregisters each object in the map. If `pCLSID` is not NULL, then only the object referred to by `pCLSID` is unregistered; otherwise all of the objects are unregistered.  
  
 This function is obsolete. Instead, use its replacement, [AtlComModuleUnregisterServer](../vs140/AtlComModuleUnregisterServer.md).  
  
 This helper function is used by [CComModule::UnregisterServer](../vs140/CComModule--UnregisterServer.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Server Registration Global Functions](../vs140/Server-Registration-Global-Functions.md)   
 [CComModule::UnregisterServer](../vs140/CComModule--UnregisterServer.md)   
 [AtlComModuleUnregisterServer](../vs140/AtlComModuleUnregisterServer.md)