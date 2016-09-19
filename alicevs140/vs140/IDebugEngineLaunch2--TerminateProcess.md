---
title: "IDebugEngineLaunch2::TerminateProcess"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f7039e7f-5f57-4222-9ad2-11a66b2da6e0
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngineLaunch2::TerminateProcess
Terminates a process.  
  
## Syntax  
  
```cpp#  
HRESULT TerminateProcess (   
   IDebugProcess2* pProcess  
);  
```  
  
```c#  
int TerminateProcess (   
   IDebugProcess2 pProcess  
);  
```  
  
#### Parameters  
 `pProcess`  
 [in] An [IDebugProcess2](../vs140/IDebugProcess2.md) object that represents the process to be terminated.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code.  
  
## Remarks  
 Call the [IDebugEngineLaunch2::CanTerminateProcess](../vs140/IDebugEngineLaunch2--CanTerminateProcess.md) method before calling this method.  
  
## See Also  
 [IDebugEngineLaunch2](../vs140/IDebugEngineLaunch2.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [IDebugEngineLaunch2::CanTerminateProcess](../vs140/IDebugEngineLaunch2--CanTerminateProcess.md)