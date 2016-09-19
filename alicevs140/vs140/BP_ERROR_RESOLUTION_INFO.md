---
title: "BP_ERROR_RESOLUTION_INFO"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a6b83242-5728-4716-80f3-840c96d59c6c
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_ERROR_RESOLUTION_INFO
Describes the resolution of an error breakpoint, including location, program, and thread.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_ERROR_RESOLUTION_INFO {   
   BPERESI_FIELDS         dwFields;  
   BP_RESOLUTION_LOCATION bpResLocation;  
   IDebugProgram2*        pProgram;  
   IDebugThread2*         pThread;  
   BSTR                   bstrMessage;  
   BP_ERROR_TYPE          dwType;  
} BP_ERROR_RESOLUTION_INFO;  
```  
  
```c#  
public struct BP_ERROR_RESOLUTION_INFO {   
   public uint                   dwFields;  
   public BP_RESOLUTION_LOCATION bpResLocation;  
   public IDebugProgram2         pProgram;  
   public IDebugThread2          pThread;  
   public string                 bstrMessage;  
   public uint                   dwType;  
};  
```  
  
## Members  
 `dwFields`  
 A combination of values from the [BPERESI_FIELDS](../vs140/BPERESI_FIELDS.md) enumeration specifying which fields of this structure are filled out.  
  
 `bpResLocation`  
 The [BP_RESOLUTION_LOCATION](../vs140/BP_RESOLUTION_LOCATION.md) union, which specifies the breakpoint resolution location.  
  
 `pProgram`  
 The [IDebugProgram2](../vs140/IDebugProgram2.md) object that represents the application in which the breakpoint error occurred.  
  
 `pThread`  
 The [IDebugThread2](../vs140/IDebugThread2.md) object that represents the thread on which the application that generated the breakpoint error is running.  
  
 `bstrMessage`  
 A string containing any warning or error message resulting from this error resolution.  
  
 `dwType`  
 A value from the [BP_ERROR_TYPE](../vs140/BP_ERROR_TYPE.md) enumeration that specifies the breakpoint error type.  
  
## Remarks  
 This structure is returned from the [GetResolutionInfo](../vs140/IDebugErrorBreakpointResolution2--GetResolutionInfo.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [GetResolutionInfo](../vs140/IDebugErrorBreakpointResolution2--GetResolutionInfo.md)   
 [BPRESI_FIELDS](../vs140/BPRESI_FIELDS.md)   
 [BP_RESOLUTION_LOCATION](../vs140/BP_RESOLUTION_LOCATION.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [BP_ERROR_TYPE](../vs140/BP_ERROR_TYPE.md)