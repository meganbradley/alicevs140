---
title: "IDebugErrorBreakpoint2::GetBreakpointResolution"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c2324ed-2a11-4e63-8f3a-f420c7a4018b
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugErrorBreakpoint2::GetBreakpointResolution
Gets the breakpoint error resolution that describes the error.  
  
## Syntax  
  
```cpp#  
HRESULT GetBreakpointResolution(   
   IDebugErrorBreakpointResolution2** ppErrorResolution  
);  
```  
  
```c#  
int GetBreakpointResolution(   
   out IDebugErrorBreakpointResolution2 ppErrorResolution  
);  
```  
  
#### Parameters  
 `ppErrorResolution`  
 [out] Returns an [IDebugErrorBreakpointResolution2](../vs140/IDebugErrorBreakpointResolution2.md) object that describes the error.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md)   
 [IDebugErrorBreakpointResolution2](../vs140/IDebugErrorBreakpointResolution2.md)