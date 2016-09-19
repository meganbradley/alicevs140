---
title: "IEnumDebugFrameInfo2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 994e30ad-435a-4f9e-9272-d96d9e01099c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugFrameInfo2
This interface enumerates [FRAMEINFO](../vs140/FRAMEINFO.md) structures.  
  
## Syntax  
  
```  
IEnumDebugFrameInfo2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to provide a list of structures that describes the current call stack.  
  
## Notes for Callers  
 Visual Studio calls [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md) to obtain this interface whenever a breakpoint, exception, or halt occurs in a program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugFrameInfo2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugFrameInfo2--Next.md)|Retrieves a specified number of [FRAMEINFO](../vs140/FRAMEINFO.md) structures in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugFrameInfo2--Skip.md)|Skips a specified number of [FRAMEINFO](../vs140/FRAMEINFO.md) structures in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugFrameInfo2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugFrameInfo2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugFrameInfo2--GetCount.md)|Gets the number of [FRAMEINFO](../vs140/FRAMEINFO.md) structures in an enumerator.|  
  
## Remarks  
 Visual Studio obtains this interface as the first step to handling a breakpoint, exception, or user-generated pause on the program being debugged. The list of [FRAMEINFO](../vs140/FRAMEINFO.md) structures represents the current call stack, with the current function call at the beginning of the list and the oldest function call at the end of the list. Each `FRAMEINFO` represents a stack frame, a context in which expressions can be evaluated and local variables looked at.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md)   
 [FRAMEINFO](../vs140/FRAMEINFO.md)