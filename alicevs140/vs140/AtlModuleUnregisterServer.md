---
title: "AtlModuleUnregisterServer"
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
ms.assetid: 9aa9c1bc-761f-498a-b53c-772cf589d4ac
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlModuleUnregisterServer
Unregisters every object in the object map. It is similar to `AtlModuleUnregisterServerEx` except that it cannot unregister the type library.  
  
 **Note** This function is obsolete in Visual C++ .NET 2002 and later but is available for backward compatibility with projects created with previous versions of Visual C++.  
  
## Syntax  
  
```  
  
      ATLAPI AtlModuleUnregisterServerEx(  
   _ATL_MODULE* pM,  
   const CLSID* pCLSID   
);  
```  
  
#### Parameters  
 `pM`  
 Pointer to a `CComModule` class or derived class.  
  
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