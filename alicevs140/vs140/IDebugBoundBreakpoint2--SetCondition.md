---
title: "IDebugBoundBreakpoint2::SetCondition"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5d366876-efed-43d0-8ea1-dfdb009cbfac
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBoundBreakpoint2::SetCondition
Sets or changes the condition associated with this bound breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT SetCondition(   
   BP_CONDITION bpCondition  
);  
```  
  
```c#  
int SetCondition(   
   enum_BP_CONDITION bpCondition  
);  
```  
  
#### Parameters  
 `bpCondition`  
 [in] A value from the [BP_CONDITION](../vs140/BP_CONDITION.md) enumeration that describes the condition.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_BP_DELETED` if the state of the bound breakpoint object is set to `BPS_DELETED` (part of the [BP_STATE](../vs140/BP_STATE.md) enumeration).  
  
## Remarks  
 Any condition that was previously associated with this breakpoint is lost.  
  
## See Also  
 [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md)   
 [BP_CONDITION](../vs140/BP_CONDITION.md)   
 [BP_STATE](../vs140/BP_STATE.md)