---
title: "IDebugPort2::GetProcess"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e2431b0-0e19-450d-8e1d-d7c314c8f872
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPort2::GetProcess
Gets the specified process running on a port.  
  
## Syntax  
  
```cpp#  
HRESULT GetProcess(   
   AD_PROCESS_ID    ProcessId,  
   IDebugProcess2** ppProcess  
);  
```  
  
```c#  
int GetProcess(   
   AD_PROCESS_ID      ProcessId,  
   out IDebugProcess2 ppProcess  
);  
```  
  
#### Parameters  
 `ProcessId`  
 [in] An [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md) structure that specifies the process identifier.  
  
 `ppProcess`  
 [out] Returns an [IDebugProcess2](../vs140/IDebugProcess2.md) object representing the process.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugPort2](../vs140/IDebugPort2.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)   
 [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md)