---
title: "IDebugDocumentPosition2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0e838ced-12bb-4efc-b811-2b7c034b77b0
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocumentPosition2
This interface represents an abstract position in a source file.  
  
## Syntax  
  
```  
IDebugDocumentPosition2 : IUnknown  
```  
  
## Notes for Implementers  
 Visual Studio typically implements this interface. A debug engine (DE) would also implement this interface if it must supply its own source code (as when the DE implements the [IDebugDocument2](../vs140/IDebugDocument2.md) interface).  
  
## Notes for Callers  
 This interface is passed in as an argument to [IDebugProgram2::EnumCodeContexts](../vs140/IDebugProgram2--EnumCodeContexts.md). It is also supplied as part of a [BP_LOCATION](../vs140/BP_LOCATION.md) union (specifically, a [BP_LOCATION_CODE_FILE_LINE](../vs140/BP_LOCATION_CODE_FILE_LINE.md) structure) that is in turn part of the [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) structure, that is used in creating a pending breakpoint.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugDocumentPosition2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetFileName](../vs140/IDebugDocumentPosition2--GetFileName.md)|Gets the file name of the source file that contains this document position.|  
|[GetDocument](../vs140/IDebugDocumentPosition2--GetDocument.md)|Gets the containing document.|  
|[IsPositionInDocument](../vs140/IDebugDocumentPosition2--IsPositionInDocument.md)|Determines if this position is contained in the given document.|  
|[GetRange](../vs140/IDebugDocumentPosition2--GetRange.md)|Gets the range for this document position.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [EnumCodeContexts](../vs140/IDebugProgram2--EnumCodeContexts.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [BP_LOCATION_CODE_FILE_LINE](../vs140/BP_LOCATION_CODE_FILE_LINE.md)