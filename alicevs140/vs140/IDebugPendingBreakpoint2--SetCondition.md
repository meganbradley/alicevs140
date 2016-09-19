---
title: "IDebugPendingBreakpoint2::SetCondition"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0534224f-654f-4862-bc4d-a9a81a5f8899
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPendingBreakpoint2::SetCondition
Sets or changes the condition associated with the pending breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT SetCondition(   
   BP_CONDITION bpCondition  
);  
```  
  
```c#  
int SetCondition(   
   BP_CONDITION bpCondition  
);  
```  
  
#### Parameters  
 `bpCondition`  
 [in] A [BP_CONDITION](../vs140/BP_CONDITION.md) structure that specifies the condition to set.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Any condition that was previously associated with the pending breakpoint is lost. All breakpoints bound from this pending breakpoint are called to set their condition to the value specified in the `bpCondition` parameter.  
  
## See Also  
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [BP_CONDITION](../vs140/BP_CONDITION.md)