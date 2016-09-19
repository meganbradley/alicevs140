---
title: "IDebugBoundBreakpoint2::GetHitCount"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 23481f37-047c-41d2-8286-4da1f4084961
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBoundBreakpoint2::GetHitCount
Gets the current hit count for this bound breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT GetHitCount(   
   DWORD* pdwHitCount  
);  
```  
  
```c#  
int GetHitCount(   
   out uint pdwHitCount  
);  
```  
  
#### Parameters  
 `pdwHitCount`  
 [out] Returns the hit count.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_BP_DELETED` if the state of the bound breakpoint object is set to `BPS_DELETED` (part of the [BP_STATE](../vs140/BP_STATE.md) enumeration).  
  
## Remarks  
 The hit count is the number of times this breakpoint has fired during the current run of the session.  
  
## See Also  
 [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md)   
 [BP_STATE](../vs140/BP_STATE.md)