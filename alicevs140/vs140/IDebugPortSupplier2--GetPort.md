---
title: "IDebugPortSupplier2::GetPort"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d55d5055-7386-4037-bf22-4c3e434a99ca
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortSupplier2::GetPort
Gets a port from a port supplier.  
  
## Syntax  
  
```cpp#  
HRESULT GetPort(   
   REFGUID       guidPort,  
   IDebugPort2** ppPort  
);  
```  
  
```c#  
int GetPort(   
   ref Guid        guidPort,  
   out IDebugPort2 ppPort  
);  
```  
  
#### Parameters  
 `guidPort`  
 [in] Globally unique identifier (GUID) of the port.  
  
 `ppPort`  
 [out] Returns an [IDebugPort2](../vs140/IDebugPort2.md) object that represents the port.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_PORTSUPPLIER_NO_PORT` if no port exists with the given identifier.  
  
## See Also  
 [IDebugPortSupplier2](../vs140/IDebugPortSupplier2.md)   
 [IDebugPort2](../vs140/IDebugPort2.md)