---
title: "IDebugStackFrame2::GetCodeContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 93d66159-a41d-49ef-982f-91bb4d073b74
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame2::GetCodeContext
Gets the code context for this stack frame.  
  
## Syntax  
  
```cpp#  
HRESULT GetCodeContext (   
   IDebugCodeContext2** ppCodeCxt  
);  
```  
  
```c#  
int GetCodeContext (   
   out IDebugCodeContext2 ppCodeCxt  
);  
```  
  
#### Parameters  
 `ppCodeCxt`  
 [out] Returns an [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object that represents the current instruction pointer in this stack frame.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)