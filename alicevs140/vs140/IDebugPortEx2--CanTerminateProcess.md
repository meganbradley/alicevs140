---
title: "IDebugPortEx2::CanTerminateProcess"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 111f65d8-5a1a-42b3-9de3-dd9bb03a33fd
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortEx2::CanTerminateProcess
Determines whether a process can be terminated.  
  
## Syntax  
  
```cpp#  
HRESULT CanTerminateProcess(   
   IDebugProcess2* pPortProcess  
);  
```  
  
```c#  
HRESULT CanTerminateProcess(   
   IDebugProcess2 pPortProcess  
);  
```  
  
#### Parameters  
 `pPortProcess`  
 [in] An [IDebugProcess2](../vs140/IDebugProcess2.md) object representing the process to be terminated.  
  
## Return Value  
 Returns `S_OK` if the process can be terminated; otherwise, returns `S_FALSE`.  
  
## See Also  
 [IDebugPortEx2](../vs140/IDebugPortEx2.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)