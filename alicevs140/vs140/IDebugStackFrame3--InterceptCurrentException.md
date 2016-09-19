---
title: "IDebugStackFrame3::InterceptCurrentException"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 116c7324-7645-4c15-b484-7a5cdd065ef5
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame3::InterceptCurrentException
Called by the debugger on the current stack frame when it wants to intercept the current exception.  
  
## Syntax  
  
```cpp  
HRESULT InterceptCurrentException(  
   INTERCEPT_EXCEPTION_ACTION dwFlags,  
   UINT64*                    pqwCookie  
);  
```  
  
```c#  
int InterceptCurrentException(  
   uint dwFlags,   
   out  ulong pqwCookie  
);  
```  
  
#### Parameters  
 `dwFlags`  
 [in] Specifies different actions. Currently, only the [INTERCEPT_EXCEPTION_ACTION](../vs140/INTERCEPT_EXCEPTION_ACTION.md) value `IEA_INTERCEPT` is supported and must be specified.  
  
 `pqwCookie`  
 [out] Unique value identifying a particular exception.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
 The following are the most common error returns.  
  
|Error|Description|  
|-----------|-----------------|  
|`E_EXCEPTION_CANNOT_BE_INTERCEPTED`|The current exception cannot be intercepted.|  
|`E_EXCEPTION_CANNOT_UNWIND_ABOVE_CALLBACK`|The current execution frame hasn't been searched for a handler yet.|  
|`E_INTERCEPT_CURRENT_EXCEPTION_NOT_SUPPORTED`|This method is not supported for this frame.|  
  
## Remarks  
 When an exception is thrown, the debugger gains control from the run time at key points during the exception handling process. During these key moments, the debugger can ask the current stack frame if the frame wants to intercept the exception. In this way, an intercepted exception is essentially an on-the-fly exception handler for a stack frame, even if that stack frame doesn't have an exception handler (for example, a try/catch block in the program code).  
  
 When the debugger wants to know if the exception should be intercepted, it calls this method on the current stack frame object. This method is responsible for handling all details of the exception. If the [IDebugStackFrame3](../vs140/IDebugStackFrame3.md) interface is not implemented or the `InterceptStackException` method returns any error, then the debugger continues processing the exception normally.  
  
> [!NOTE]
>  Exceptions can be intercepted only in managed code, that is, when the program being debugged is running under the .NET run time. Of course, third-party language implementers can implement `InterceptStackException` in their own debug engines if they so choose.  
  
 After the interception is complete, an [IDebugInterceptExceptionCompleteEvent2](../vs140/IDebugInterceptExceptionCompleteEvent2.md) is signaled.  
  
## See Also  
 [IDebugStackFrame3](../vs140/IDebugStackFrame3.md)   
 [INTERCEPT_EXCEPTION_ACTION](../vs140/INTERCEPT_EXCEPTION_ACTION.md)   
 [IDebugInterceptExceptionCompleteEvent2](../vs140/IDebugInterceptExceptionCompleteEvent2.md)