---
title: "IDebugCanStopEvent2::GetCodeContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eecf08b6-f9b7-4358-941b-3a448a92ac62
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCanStopEvent2::GetCodeContext
Gets the code context that describes the location of this event.  
  
## Syntax  
  
```cpp#  
HRESULT GetCodeContext(   
   IDebugCodeContext2** ppCodeContext  
);  
```  
  
```c#  
int GetCodeContext(   
   out IDebugCodeContext2 ppCodeContext  
);  
```  
  
#### Parameters  
 `ppCodeContext`  
 [out] Returns the [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object that represents the current code location.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 For most run-time architectures, a code context can be thought of as an address in a program's execution stream, pointing to a specific instruction.  
  
 To get the document context, which is oriented towards lines of source code, call the [IDebugCanStopEvent2::GetDocumentContext](../vs140/IDebugCanStopEvent2--GetDocumentContext.md) method.  
  
## See Also  
 [IDebugCanStopEvent2](../vs140/IDebugCanStopEvent2.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)   
 [IDebugCanStopEvent2::GetDocumentContext](../vs140/IDebugCanStopEvent2--GetDocumentContext.md)