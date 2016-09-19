---
title: "IDebugErrorBreakpoint2::GetPendingBreakpoint"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59d0defc-99fd-445c-bdac-8224d5dea3f9
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugErrorBreakpoint2::GetPendingBreakpoint
Gets the pending breakpoint that caused the error.  
  
## Syntax  
  
```cpp#  
HRESULT GetPendingBreakpoint (   
   IDebugPendingBreakpoint2** ppPendingBreakpoint  
);  
```  
  
```c#  
int GetPendingBreakpoint (   
   out IDebugPendingBreakpoint2 ppPendingBreakpoint  
);  
```  
  
#### Parameters  
 `ppPendingBreakpoint`  
 [out] Returns an [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) object that represents the pending breakpoint that failed to be bound.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)