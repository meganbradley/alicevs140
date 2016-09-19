---
title: "AtlModuleRegisterTypeLib"
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
ms.assetid: 095cf576-f122-4a05-89e3-0e1d12f8ccc8
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlModuleRegisterTypeLib
Registers a type library.  
  
 **Note** This function is obsolete in Visual C++ .NET 2002 and later but is available for backward compatibility with projects created with previous versions of Visual C++.  
  
## Syntax  
  
```  
  
      ATLAPI AtlModuleRegisterTypeLib(  
   _ATL_MODULE* pM,  
   LPCOLESTR lpszIndex   
);  
```  
  
#### Parameters  
 `pM`  
 Pointer to a `CComModule` class or derived class.  
  
 `lpszIndex`  
 String in the format "\\\N", where N is the integer index of the type library resource. Can be NULL if no index is required.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This function is obsolete. Instead, use its replacement, [AtlRegisterTypeLib](../vs140/AtlRegisterTypeLib.md).  
  
 This helper function is used by [CComModule::RegisterTypeLib](../vs140/CComModule--RegisterTypeLib.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [Server Registration Global Functions](../vs140/Server-Registration-Global-Functions.md)   
 [CComModule::RegisterTypeLib](../vs140/CComModule--RegisterTypeLib.md)