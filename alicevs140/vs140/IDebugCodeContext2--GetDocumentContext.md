---
title: "IDebugCodeContext2::GetDocumentContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d552cc92-963f-43c1-949f-ae6b63a427b8
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCodeContext2::GetDocumentContext
Gets the document context that corresponds to this code context. The document context represents a position in the source file that corresponds to the source code that generated this instruction.  
  
## Syntax  
  
```cpp#  
HRESULT GetDocumentContext(   
   IDebugDocumentContext2** ppSrcCxt  
);  
```  
  
```c#  
int GetDocumentContext(   
   out IDebugDocumentContext2 ppSrcCxt  
);  
```  
  
#### Parameters  
 `ppSrcCxt`  
 [out] Returns the [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md) object that corresponds to the code context.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Generally, the document context can be thought of as a position in a source file while the code context is a position of a code instruction in an execution stream.  
  
## See Also  
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)   
 [IDebugDocumentContext2](../vs140/IDebugDocumentContext2.md)