---
title: "IDebugCanStopEvent2::GetDocumentContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 936a6c4e-30c5-4c7e-9ad5-910cc605a4b5
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCanStopEvent2::GetDocumentContext
Gets the document context that describes the location of this event.  
  
## Syntax  
  
```cpp#  
HRESULT GetDocumentContext (   
   IDebugDocumentContext2** ppDocCxt  
);  
```  
  
```c#  
int GetDocumentContext (   
   out IDebugDocumentContext2 ppDocCxt  
);  
```  
  
#### Parameters  
 `ppDocCxt`  
 [out] Returns the [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md) interface that represents a position in a source file document corresponding to the current code location.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Generally, the document context can be thought of as a position in a source file.  
  
 To get the code context, which is oriented towards code instructions, call the [IDebugCanStopEvent2::GetCodeContext](../vs140/IDebugCanStopEvent2--GetCodeContext.md) method.  
  
## See Also  
 [IDebugCanStopEvent2](../vs140/IDebugCanStopEvent2.md)   
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)   
 [IDebugCanStopEvent2::GetCodeContext](../vs140/IDebugCanStopEvent2--GetCodeContext.md)