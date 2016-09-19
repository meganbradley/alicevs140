---
title: "IDebugDocumentContext2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2a446c71-8100-4c09-a1cc-fd446bd74030
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentContext2
This interface represents a position in a source file document.  
  
## Syntax  
  
```  
IDebugDocumentContext2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for source code level debugging. In addition to a position in source code, this interface supplies methods for comparing contexts and navigating through a source code document.  
  
## Notes for Callers  
 Methods on several interfaces, most typically the [IDebugStackFrame2::GetDocumentContext](../vs140/IDebugStackFrame2--GetDocumentContext.md) and [IDebugCodeContext2::GetDocumentContext](../vs140/IDebugCodeContext2--GetDocumentContext.md) interfaces, return this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugDocumentContext2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetDocument](../vs140/IDebugDocumentContext2--GetDocument.md)|Gets the document that contains this document context.|  
|[GetName](../vs140/IDebugDocumentContext2--GetName.md)|Gets the displayable name of the document that contains this document context.|  
|[EnumCodeContexts](../vs140/IDebugDocumentContext2--EnumCodeContexts.md)|Retrieves a list of all code contexts associated with this document context.|  
|[GetLanguageInfo](../vs140/IDebugDocumentContext2--GetLanguageInfo.md)|Gets the language associated with this document context.|  
|[GetStatementRange](../vs140/IDebugDocumentContext2--GetStatementRange.md)|Gets the file statement range of this document context.|  
|[GetSourceRange](../vs140/IDebugDocumentContext2--GetSourceRange.md)|Gets the file source range of this document context.|  
|[Compare](../vs140/IDebugDocumentContext2--Compare.md)|Compares this document context to a given array of document contexts.|  
|[Seek](../vs140/IDebugDocumentContext2--Seek.md)|Moves the document context by a given number of statements or lines.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [GetDocumentContext](../vs140/IDebugCanStopEvent2--GetDocumentContext.md)   
 [GetDocumentContext](../vs140/IDebugActivateDocumentEvent2--GetDocumentContext.md)   
 [GetDocumentContext](../vs140/IDebugStackFrame2--GetDocumentContext.md)   
 [GetDocumentContext](../vs140/IDebugCodeContext2--GetDocumentContext.md)