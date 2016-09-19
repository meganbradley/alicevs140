---
title: "IDebugDefaultPort2::GetServer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cacb4b74-0f39-471c-af38-54b73f5b2868
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDefaultPort2::GetServer
This method obtains an interface to the server that this port is on.  
  
## Syntax  
  
```cpp  
HRESULT GetServer(  
   IDebugCoreServer3** ppServer  
);  
```  
  
```c#  
int GetServer(  
   out IDebugCoreServer3 ppServer  
);  
```  
  
#### Parameters  
 `ppServer`  
 [out] Returns an object implementing the [IDebugCoreServer3](../vs140/IDebugCoreServer3.md) interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The [IDebugCoreServer3](../vs140/IDebugCoreServer3.md) is implemented by Visual Studio and represents the server that the port is located on.  
  
## See Also  
 [IDebugDefaultPort2](../vs140/IDebugDefaultPort2.md)   
 [IDebugCoreServer3](../vs140/IDebugCoreServer3.md)