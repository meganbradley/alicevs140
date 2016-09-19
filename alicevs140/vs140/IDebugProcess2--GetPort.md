---
title: "IDebugProcess2::GetPort"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e39b6e5a-64eb-48cf-a53d-da4fdb968e2d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::GetPort
Gets the port that the process is running on.  
  
## Syntax  
  
```cpp#  
HRESULT GetPort(   
   IDebugPort2** ppPort  
);  
```  
  
```c#  
int GetPort(   
   out IDebugPort2 ppPort  
);  
```  
  
#### Parameters  
 `ppPort`  
 [out] Returns an [IDebugPort2](../vs140/IDebugPort2.md) object that represents the port on which the process was launched.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [IDebugPort2](../vs140/IDebugPort2.md)