---
title: "IDebugBoundBreakpoint2::SetPassCount"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b32c12f9-b34d-43bd-a1b9-61af6cf8e51b
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBoundBreakpoint2::SetPassCount
Sets or changes the pass count associated with this bound breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT SetPassCount(   
   BP_PASSCOUNT bpPassCount  
);  
```  
  
```c#  
int SetPassCount(   
   BP_PASSCOUNT bpPassCount  
);  
```  
  
#### Parameters  
 `bpPassCount`  
 [in] The [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md) structure that specifies the pass count.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_BP_DELETED` if the state of the bound breakpoint object is set to `BPS_DELETED` (part of the [BP_STATE](../vs140/BP_STATE.md) enumeration).  
  
## Remarks  
 The pass count determines when the breakpoint is fired. The current pass or hit count can be obtained by calling the [IDebugBoundBreakpoint2::GetHitCount](../vs140/IDebugBoundBreakpoint2--GetHitCount.md) method.  
  
 Any pass count that was previously associated with this breakpoint is lost.  
  
## See Also  
 [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md)   
 [IDebugBoundBreakpoint2::GetHitCount](../vs140/IDebugBoundBreakpoint2--GetHitCount.md)   
 [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md)   
 [BP_STATE](../vs140/BP_STATE.md)