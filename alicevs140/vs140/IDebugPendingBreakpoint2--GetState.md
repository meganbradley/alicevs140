---
title: "IDebugPendingBreakpoint2::GetState"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e88d543f-2e83-4ba7-86ca-f874e39955ff
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPendingBreakpoint2::GetState
Gets the state of the pending breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT GetState(   
   PENDING_BP_STATE_INFO* pState  
);  
```  
  
```c#  
int GetState(   
   PENDING_BP_STATE_INFO[] pState  
);  
```  
  
#### Parameters  
 `pState`  
 [in, out] A [PENDING_BP_STATE_INFO](../vs140/PENDING_BP_STATE_INFO.md) structure that is filled in with a description of this pending breakpoint.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [PENDING_BP_STATE_INFO](../vs140/PENDING_BP_STATE_INFO.md)