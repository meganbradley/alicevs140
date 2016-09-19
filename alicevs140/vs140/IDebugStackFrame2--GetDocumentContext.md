---
title: "IDebugStackFrame2::GetDocumentContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69e81439-1238-4f18-9028-6fd1c1ba5e4a
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame2::GetDocumentContext
Gets the document context for this stack frame.  
  
## Syntax  
  
```cpp#  
HRESULT GetDocumentContext (   
   IDebugDocumentContext2** ppCxt  
);  
```  
  
```c#  
int GetDocumentContext (   
   out IDebugDocumentContext2 ppCxt  
);  
```  
  
#### Parameters  
 `ppCxt`  
 [out] Returns an [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md) object that represents the current position in a source document.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is faster than calling the [IDebugStackFrame2::GetCodeContext](../vs140/IDebugStackFrame2--GetCodeContext.md) method and then calling the [IDebugCodeContext2::GetDocumentContext](../vs140/IDebugCodeContext2--GetDocumentContext.md) method on the code context. However, it is not guaranteed that every debug engine (DE) will implement this method.  
  
## See Also  
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)   
 [IDebugCodeContext2::GetDocumentContext](../vs140/IDebugCodeContext2--GetDocumentContext.md)   
 [IDebugStackFrame2::GetCodeContext](../vs140/IDebugStackFrame2--GetCodeContext.md)