---
title: "IDebugCoreServer3::CreateInstanceInServer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76f36bae-f6ab-413c-a8a9-8808bfeba05b
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer3::CreateInstanceInServer
Creates an instance of a debug engine on the server.  
  
## Syntax  
  
```cpp#  
HRESULT CreateInstanceInServer(  
   LPCWSTR  szDll,  
   WORD     wLangId,  
   REFCLSID clsidObject,  
   REFIID   riid,  
   void**   ppvObject  
);  
```  
  
```c#  
int CreateInstanceInServer(  
   string     szDll,   
   ushort     wLangID,   
   ref Guid   clsidObject,   
   ref Guid   riid,   
   out IntPtr ppvObject  
);  
```  
  
#### Parameters  
 `szDll`  
 [in] Path to the dll that implements the CLSID specified in the `clsidObject` parameter. If this is `NULL`, then COM's `CoCreateInstance` function is called.  
  
 `wLangId`  
 [in] Locale of the debug engine. This can be 0 if the [IDebugEngine2::SetLocale](../vs140/IDebugEngine2--SetLocale.md) method should not be called.  
  
 `clsidObject`  
 [in] CLSID of the debug engine to create.  
  
 `riid`  
 [in] Interface ID of the specific interface to retrieve from the class object.  
  
 `ppvObject`  
 [out] `IUnknown` interface from the instantiated object. Cast or marshal this object to the desired interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugCoreServer3](../vs140/IDebugCoreServer3.md)   
 [IDebugEngine2::SetLocale](../vs140/IDebugEngine2--SetLocale.md)