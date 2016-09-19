---
title: "IDebugProgramHost2::GetHostId"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7702e221-feb1-446b-a224-cb46c420987e
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramHost2::GetHostId
Gets the process identifier of the process hosting this program.  
  
## Syntax  
  
```cpp#  
HRESULT GetHostId(   
   AD_PROCESS_ID* pdwId  
);  
```  
  
```c#  
int GetHostId(   
   AD_PROCESS_ID[] pdwId  
);  
```  
  
#### Parameters  
 `pdwId`  
 [in, out] An [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md) structure that is filled in with the process identifier information.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProgramHost2](../vs140/IDebugProgramHost2.md)   
 [AD_PROCESS_ID](../vs140/AD_PROCESS_ID.md)