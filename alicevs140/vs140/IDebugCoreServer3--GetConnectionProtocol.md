---
title: "IDebugCoreServer3::GetConnectionProtocol"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 368ced5b-c5d9-4090-a5b4-26ff400d1a55
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer3::GetConnectionProtocol
Returns a value indicating the protocol that is being used to communicate between the server and the debug package.  
  
## Syntax  
  
```cpp#  
HRESULT GetConnectionProtocol(  
   CONNECTION_PROTOCOL* pProtocol  
);  
```  
  
```c#  
int GetConnectionProtocol(  
   CONNECTION_PROTOCOL[] pProtocol  
);  
```  
  
#### Parameters  
 `pProtocol`  
 [out] Returns one of the values from the [CONNECTION_PROTOCOL](../vs140/CONNECTION_PROTOCOL.md) enumeration.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## See Also  
 [IDebugCoreServer3](../vs140/IDebugCoreServer3.md)   
 [CONNECTION_PROTOCOL](../vs140/CONNECTION_PROTOCOL.md)