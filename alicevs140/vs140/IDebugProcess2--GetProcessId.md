---
title: "IDebugProcess2::GetProcessId"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d5b6f03c-d49d-4b83-b072-016ac3124f5f
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::GetProcessId
Gets the GUID for this process.  
  
## Syntax  
  
```cpp#  
HRESULT GetProcessId(  
   GUID* pguidProcessId  
);  
```  
  
```c#  
int GetProcessId(  
   out Guid pguidProcessId  
);  
```  
  
#### Parameters  
 `pguidProcessId`  
 [out] Returns the GUID for this process.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The Globally Unique IDentifier (GUID) identifies this process from all other processes running in the system.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)