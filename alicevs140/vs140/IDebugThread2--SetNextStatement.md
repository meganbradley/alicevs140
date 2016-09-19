---
title: "IDebugThread2::SetNextStatement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e2834dd-4ecf-45af-8e6c-f9318ebdac06
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThread2::SetNextStatement
Sets the current instruction pointer to the given code context.  
  
## Syntax  
  
```cpp#  
HRESULT SetNextStatement (   
   IDebugStackFrame2*  pStackFrame,  
   IDebugCodeContext2* pCodeContext  
);  
```  
  
```c#  
int SetNextStatement (   
   IDebugStackFrame2  pStackFrame,  
   IDebugCodeContext2 pCodeContext  
);  
```  
  
#### Parameters  
 `pStackFrame`  
 Reserved for future use; set to a null value.  
  
 `pCodeContext`  
 [in] An [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object that describes the code location about to be executed and its context.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following table shows other possible values.  
  
|Value|Description|  
|-----------|-----------------|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_NONLEAF_FRAME|The next statement cannot be in a stack frame deeper on the frame stack.|  
|E_CANNOT_SETIP_TO_DIFFERENT_FUNCTION|The next statement is not associated with any frame in the stack.|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_EXCEPTION|Some debug engines cannot set the next statement after an exception.|  
  
## Remarks  
 The instruction pointer indicates the next instruction or statement to execute. This method is used to retry a line of source code or to force execution to continue in another function, for example.  
  
## See Also  
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)