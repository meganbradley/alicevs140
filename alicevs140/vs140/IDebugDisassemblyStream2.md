---
title: "IDebugDisassemblyStream2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b03cab0c-3f0b-4cc6-88dc-acb3b48c567a
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDisassemblyStream2
This interface represents a stream of instructions.  
  
## Syntax  
  
```  
IDebugDisassemblyStream2 : IUnknown  
```  
  
## Notes for Implementers  
 A debug engine implements this interface to support disassembly of a program's code.  
  
## Notes for Callers  
 A call to the [IDebugProgram2::GetDisassemblyStream](../vs140/IDebugProgram2--GetDisassemblyStream.md) method returns this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugDisassemblyStream2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Read](../vs140/IDebugDisassemblyStream2--Read.md)|Reads instructions starting from the current position in the disassembly stream.|  
|[Seek](../vs140/IDebugDisassemblyStream2--Seek.md)|Moves the read pointer in the disassembly stream a given number of instructions relative to a specified position.|  
|[GetCodeLocationId](../vs140/IDebugDisassemblyStream2--GetCodeLocationId.md)|Returns a code location identifier for a particular code context.|  
|[GetCodeContext](../vs140/IDebugDisassemblyStream2--GetCodeContext.md)|Returns a code context object corresponding to a specified code location identifier.|  
|[GetCurrentLocation](../vs140/IDebugDisassemblyStream2--GetCurrentLocation.md)|Returns a code location identifier that represents the current code location.|  
|[GetDocument](../vs140/IDebugDisassemblyStream2--GetDocument.md)|Gets the source document associated with this disassembly stream.|  
|[GetScope](../vs140/IDebugDisassemblyStream2--GetScope.md)|Gets the scope of this disassembly stream.|  
|[GetSize](../vs140/IDebugDisassemblyStream2--GetSize.md)|Gets the size of this disassembly stream.|  
  
## Remarks  
 The disassembly stream can be created to represent the entire address space or just a function or module within the space. Each instruction is represented by a [DisassemblyData](../vs140/DisassemblyData.md) structure returned by a call to the [IDebugDisassemblyStream2::Read](../vs140/IDebugDisassemblyStream2--Read.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [GetDisassemblyStream](../vs140/IDebugProgram2--GetDisassemblyStream.md)   
 [DisassemblyData](../vs140/DisassemblyData.md)