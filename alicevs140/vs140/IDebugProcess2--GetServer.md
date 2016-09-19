---
title: "IDebugProcess2::GetServer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f73c530-cceb-4f1f-8c63-1cc0ccd4a310
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::GetServer
Gets the server that this process is running on.  
  
## Syntax  
  
```cpp#  
HRESULT GetServer(   
   IDebugCoreServer2** ppServer  
);  
```  
  
```c#  
int GetServer(   
   out IDebugCoreServer2 ppServer  
);  
```  
  
#### Parameters  
 `ppServer`  
 [out] Returns an [IDebugCoreServer2](../vs140/IDebugCoreServer2.md) object that represents the server on which this process is running.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 More than one server can be running on a single machine.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)