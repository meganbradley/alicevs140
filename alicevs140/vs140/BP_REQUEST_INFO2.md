---
title: "BP_REQUEST_INFO2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 008c87f7-a76e-43d3-8904-11b225d6a9a5
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_REQUEST_INFO2
Contains the information required to implement a breakpoint, including vendor GUID, constraint and tracepoint.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_REQUEST_INFO2 {  
   BPREQI_FIELDS   dwFields;  
   GUID            guidLanguage;  
   BP_LOCATION     bpLocation;  
   IDebugProgram2* pProgram;  
   BSTR            bstrProgramName;  
   IDebugThread2*  pThread;  
   BSTR            bstrThreadName;  
   BP_CONDITION    bpCondition;  
   BP_PASSCOUNT    bpPassCount;  
   BP_FLAGS        dwFlags;  
   GUID            guidVendor;  
   BSTR            bstrConstraint;  
   BSTR            bstrTracepoint;  
} BP_REQUEST_INFO2;  
```  
  
```c#  
public struct BP_REQUEST_INFO2 {  
   public uint           dwFields;  
   public Guid           guidLanguage;  
   public BP_LOCATION    bpLocation;  
   public IDebugProgram2 pProgram;  
   public string         bstrProgramName;  
   public IDebugThread2  pThread;  
   public string         bstrThreadName;  
   public BP_CONDITION   bpCondition;  
   public BP_PASSCOUNT   bpPassCount;  
   public uint           dwFlags;  
   public Guid           guidVendor;  
   public string         bstrConstraint;  
   public string         bstrTracepoint;  
};  
```  
  
## Members  
 `dwFields`  
 A combination of flags from the [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md) enumeration that specifies which fields are filled out.  
  
 `guidLanguage`  
 The language GUID.  
  
 `bpLocation`  
 The [BP_LOCATION](../vs140/BP_LOCATION.md) structure that specifies the type of the breakpoint location.  
  
 `pProgram`  
 The [IDebugProgram2](../vs140/IDebugProgram2.md) object that represents the application in which the breakpoint occurs.  
  
 `bstrProgramName`  
 The name of the application in which the breakpoint occurs.  
  
 `pThread`  
 The [IDebugThread2](../vs140/IDebugThread2.md) object that represents the thread in which the breakpoint occurs.  
  
 `bstrThreadName`  
 The name of the thread in which the breakpoint occurs.  
  
 `bpCondition`  
 The [BP_CONDITION](../vs140/BP_CONDITION.md) structure that describes the conditions under which the breakpoint will fire.  
  
 `bpPassCount`  
 The [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md) structure that contains the pass count information of the breakpoint.  
  
 `dwFlags`  
 A combination of flags from the [BP_FLAGS](../vs140/BP_FLAGS.md) enumeration that specifies the flags for the requested breakpoint.  
  
 `guidVendor`  
 GUID of vendor. May be a null value.  
  
 `bstrConstraint`  
 Name of breakpoint constraint. May be a null value.  
  
 `bstrTracepoint`  
 Name of trace point. May be a null value.  
  
## Remarks  
 This structure is returned by the [IDebugBreakpointRequest3::GetRequestInfo2](../vs140/IDebugBreakpointRequest3--GetRequestInfo2.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [IDebugBreakpointRequest3::GetRequestInfo2](../vs140/IDebugBreakpointRequest3--GetRequestInfo2.md)   
 [BPREQI_FIELDS](../vs140/BPREQI_FIELDS.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [BP_CONDITION](../vs140/BP_CONDITION.md)   
 [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md)   
 [BP_FLAGS](../vs140/BP_FLAGS.md)