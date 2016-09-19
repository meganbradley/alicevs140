---
title: "IEnumDebugCodeContexts2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 72915146-215f-4c99-a034-131b2b474e0e
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugCodeContexts2
This interface enumerates the code contexts associated with the debug session, or with a particular program or document.  
  
## Syntax  
  
```  
IEnumDebugCodeContexts2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a list of code contexts for a particular text position in a program, or a list of code contexts for a particular document context.  
  
## Notes for Callers  
 Call [IDebugProgram2::EnumCodeContexts](../vs140/IDebugProgram2--EnumCodeContexts.md) to obtain this interface representing a list of code contexts for a specific text position in a program's source document.  
  
 Call [IDebugDocumentContext2::EnumCodeContexts](../vs140/IDebugDocumentContext2--EnumCodeContexts.md) to obtain this interface representing a list of all code contexts in a particular source document.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugCodeContexts2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugCodeContexts2--Next.md)|Retrieves a specified number of code contexts in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugCodeContexts2--Skip.md)|Skips a specified number of code contexts in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugCodeContexts2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugCodeContexts2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugCodeContexts2--GetCount.md)|Gets the number of code contexts in an enumerator.|  
  
## Remarks  
 Visual Studio calls [IDebugProgram2::EnumCodeContexts](../vs140/IDebugProgram2--EnumCodeContexts.md) to populate a list of code contexts the user can choose from when setting the next statement or showing the disassembly for a source file. Multiple code contexts can occur, for example, when there are multiple instances of a C++-style template.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [EnumCodeContexts](../vs140/IDebugProgram2--EnumCodeContexts.md)   
 [EnumCodeContexts](../vs140/IDebugDocumentContext2--EnumCodeContexts.md)