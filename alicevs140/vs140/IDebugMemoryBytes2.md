---
title: "IDebugMemoryBytes2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7647575-0e06-4190-88f5-ca40b82209a4
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMemoryBytes2
This interface represents bytes of memory.  
  
## Syntax  
  
```  
IDebugMemoryBytes2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent bytes in memory.  
  
## Notes for Callers  
 [IDebugProgram2::GetMemoryBytes](../vs140/IDebugProgram2--GetMemoryBytes.md) returns this interface to provide access to system memory. [IDebugProperty2::GetMemoryBytes](../vs140/IDebugProperty2--GetMemoryBytes.md) and [IDebugReference2::GetMemoryBytes](../vs140/IDebugReference2--GetMemoryBytes.md) return this interface to provide access to an object's bytes.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugMemoryBytes2`.  
  
|Method|Description|  
|------------|-----------------|  
|[ReadAt](../vs140/IDebugMemoryBytes2--ReadAt.md)|Reads a sequence of bytes, starting at a given location.|  
|[WriteAt](../vs140/IDebugMemoryBytes2--WriteAt.md)|Writes `dwCount` bytes, starting at `pStartContext`.|  
|[GetSize](../vs140/IDebugMemoryBytes2--GetSize.md)|Gets the size, in bytes, of the memory represented by this interface.|  
  
## Remarks  
 For properties, an [IDebugProperty2](../vs140/IDebugProperty2.md) interface representing an array provides an `IDebugMemoryBytes2` interface to access the values in that array.  
  
 Visual Studio's **Memory View** calls [IDebugProgram2::GetMemoryBytes](../vs140/IDebugProgram2--GetMemoryBytes.md) to retrieve an `IDebugMemoryBytes2` interface for accessing system memory. The address to be accessed is obtained by parsing the expression entered as an address into the Memory View and then evaluating the parsed expression using [IDebugExpression2::EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md) to get an `IDebugProperty2` interface. A call to [IDebugProperty2::GetMemoryContext](../vs140/IDebugProperty2--GetMemoryContext.md) returns the [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md) that describes the memory address. This memory context is then passed to [IDebugMemoryBytes2::ReadAt](../vs140/IDebugMemoryBytes2--ReadAt.md) and [IDebugMemoryBytes2::WriteAt](../vs140/IDebugMemoryBytes2--WriteAt.md).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [GetMemoryBytes](../vs140/IDebugProgram2--GetMemoryBytes.md)   
 [IDebugProperty2::GetMemoryBytes](../vs140/IDebugProperty2--GetMemoryBytes.md)   
 [IDebugReference2::GetMemoryBytes](../vs140/IDebugReference2--GetMemoryBytes.md)   
 [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md)