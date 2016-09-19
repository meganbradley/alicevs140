---
title: "IDebugMemoryContext2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a544c8b-11dc-46bb-8549-261e4ac5bbc4
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMemoryContext2
This interface represents a position in the address space of the machine running the program being debugged.  
  
## Syntax  
  
```  
IDebugMemoryContext2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent an address in memory.  
  
## Notes for Callers  
 A call to [IDebugProperty2::GetMemoryContext](../vs140/IDebugProperty2--GetMemoryContext.md) or [IDebugReference2::GetMemoryContext](../vs140/IDebugReference2--GetMemoryContext.md) returns this interface. Also, calls to [IDebugMemoryContext2::Add](../vs140/IDebugMemoryContext2--Add.md) and [IDebugMemoryContext2::Subtract](../vs140/IDebugMemoryContext2--Subtract.md) return new copies of this interface after the appropriate arithmetic operation has been applied.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugMemoryContext2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetName](../vs140/IDebugMemoryContext2--GetName.md)|Gets the user-displayable name for this context.|  
|[GetInfo](../vs140/IDebugMemoryContext2--GetInfo.md)|Gets information that describes this context.|  
|[Add](../vs140/IDebugMemoryContext2--Add.md)|Adds a specified value to the current context's address to create a new context.|  
|[Subtract](../vs140/IDebugMemoryContext2--Subtract.md)|Subtracts a specified value from the current context's address to create a new context.|  
|[Compare](../vs140/IDebugMemoryContext2--Compare.md)|Compares two contexts in the manner indicated by compare flags.|  
  
## Remarks  
 Visual Studio's **Memory** window calls [IDebugProperty2::GetMemoryContext](../vs140/IDebugProperty2--GetMemoryContext.md) to obtain the `IDebugMemoryContext2` interface that contains the evaluated expression used for the memory address. This context is then passed to [IDebugMemoryBytes2::ReadAt](../vs140/IDebugMemoryBytes2--ReadAt.md) and [IDebugMemoryBytes2::WriteAt](../vs140/IDebugMemoryBytes2--WriteAt.md) to specify the address to read or write.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProperty2::GetMemoryContext](../vs140/IDebugProperty2--GetMemoryContext.md)   
 [IDebugReference2::GetMemoryContext](../vs140/IDebugReference2--GetMemoryContext.md)   
 [ReadAt](../vs140/IDebugMemoryBytes2--ReadAt.md)   
 [WriteAt](../vs140/IDebugMemoryBytes2--WriteAt.md)