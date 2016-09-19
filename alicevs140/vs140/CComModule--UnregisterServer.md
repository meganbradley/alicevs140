---
title: "CComModule::UnregisterServer"
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
ms.assetid: 41a97389-2edb-4ee7-983a-1d697c5c7554
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::UnregisterServer
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      HRESULT UnregisterServer(  
   const CLSID* pCLSID = NULL  
) throw ( );  
inline HRESULT UnregisterServer(  
   BOOL bUnRegTypeLib,  
   const CLSID* pCLSID = NULL  
) throw ( );  
```  
  
#### Parameters  
 `bUnRegTypeLib`  
 If **TRUE**, the type library is also unregistered.  
  
 `pCLSID`  
 Points to the CLSID of the object to be unregistered. If **NULL** (the default value), all objects in the object map will be unregistered.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Depending on the `pCLSID` parameter, unregisters either a single class object or all objects in the object map.  
  
 `UnregisterServer` will be called automatically by **DLLUnregisterServer** for a DLL or by `WinMain` for an EXE run with the **/UnregServer** command line option.  
  
 See [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md) for information on how to add an entry to the object map.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::RegisterServer](../vs140/CComModule--RegisterServer.md)