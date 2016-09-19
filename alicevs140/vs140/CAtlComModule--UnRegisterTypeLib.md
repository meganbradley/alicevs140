---
title: "CAtlComModule::UnRegisterTypeLib"
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
ms.assetid: dc64f1e8-e3a2-4b39-9215-b5c23816c3d0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlComModule::UnRegisterTypeLib
Call this method to unregister a type library.  
  
## Syntax  
  
```  
  
      HRESULT UnRegisterTypeLib(  
   LPCTSTR lpszIndex   
);  
HRESULT UnRegisterTypeLib( );  
```  
  
#### Parameters  
 `lpszIndex`  
 String in the format "\\\N", where N is the integer index of the TYPELIB resource.  
  
## Remarks  
 Removes information about a type library from the system registry. If the module instance contains multiple type libraries, use the first version of this method to specify which type library should be used.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlComModule Class](../vs140/CAtlComModule-Class.md)   
 [CAtlComModule::RegisterTypeLib](../vs140/CAtlComModule--RegisterTypeLib.md)