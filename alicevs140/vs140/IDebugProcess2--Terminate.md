---
title: "IDebugProcess2::Terminate"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5e6bf373-0fe9-4321-b04a-473a65f664d9
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::Terminate
Terminates the process.  
  
## Syntax  
  
```cpp#  
HRESULT Terminate(   
   void   
);  
```  
  
```c#  
int Terminate();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 When a process is terminated, all programs within that process are terminated; none are allowed to run any more code.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)