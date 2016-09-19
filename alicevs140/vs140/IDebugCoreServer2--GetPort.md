---
title: "IDebugCoreServer2::GetPort"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3f5ea4a8-6085-4600-980a-9e48f8b5be56
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer2::GetPort
Retrieves a specific port.  
  
## Syntax  
  
```cpp#  
HRESULT GetPort(   
   REFGUID       guidPort,  
   IDebugPort2** ppPort  
);  
```  
  
```c#  
int GetPort(   
   ref Guid        guidPort,  
   out IDebugPort2 ppPort  
);  
```  
  
#### Parameters  
 `guidPort`  
 [in] GUID of the port to be retrieved.  
  
 `ppPort`  
 [out] Returns an [IDebugPort2](../vs140/IDebugPort2.md) object representing the desired port.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_PORTSUPPLIER_NO_PORT` if there is no port with the given identifier.  
  
## See Also  
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)   
 [IDebugPort2](../vs140/IDebugPort2.md)