---
title: "IDebugExceptionEvent2::CanPassToDebuggee"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ae4bbe0a-fbe1-49be-a310-ea64279a434b
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExceptionEvent2::CanPassToDebuggee
Determines whether or not the debug engine (DE) supports the option of passing this exception to the program being debugged when execution resumes.  
  
## Syntax  
  
```cpp#  
HRESULT CanPassToDebuggee(  
   void  
);  
```  
  
```c#  
int CanPassToDebuggee();  
```  
  
## Return Value  
 Returns either `S_OK` (the exception can be passed to the program) or `S_FALSE` (the exception cannot be passed on).  
  
## Remarks  
 The DE must have a default action for passing to the debuggee. The IDE may receive the [IDebugExceptionEvent2](../vs140/IDebugExceptionEvent2.md) event and call the [IDebugProcess3::Continue](../vs140/IDebugProcess3--Continue.md) method without calling the `CanPassToDebuggee` method. Therefore, the DE should have a default case for passing the exception on or not.  
  
## See Also  
 [IDebugExceptionEvent2](../vs140/IDebugExceptionEvent2.md)   
 [IDebugProcess3::Continue](../vs140/IDebugProcess3--Continue.md)