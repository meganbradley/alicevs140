---
title: "Entering Break Mode"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9a8a241-cd21-4d4e-999a-283554c288b1
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Entering Break Mode
The following describes the process that occurs when a breakpoint is encountered after stepping into a function, running to the line of source code that has the cursor in it, or running to a breakpoint.  
  
## Break Mode Process  
  
1.  The debug engine (DE) sends [IDebugBreakpointEvent2](../vs140/IDebugBreakpointEvent2.md), [IDebugExceptionEvent2](../vs140/IDebugExceptionEvent2.md), or any other stopping event to cause the IDE to enter break mode.  
  
2.  The SDM gets the call stack information from the thread, as follows:  
  
    -   [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md)  
  
    -   [IEnumDebugFrameInfo2::GetCount](../vs140/IEnumDebugFrameInfo2--GetCount.md)  
  
    -   [IEnumDebugFrameInfo2::Next](../vs140/IEnumDebugFrameInfo2--Next.md)  
  
    -   [IDebugStackFrame2::GetDocumentContext](../vs140/IDebugStackFrame2--GetDocumentContext.md) to get the source code information  
  
    -   [IDebugDocumentContext2::GetName](../vs140/IDebugDocumentContext2--GetName.md) to get the file name  
  
    -   [IDebugDocumentContext2::GetStatementRange](../vs140/IDebugDocumentContext2--GetStatementRange.md) to get the statement range  
  
    -   [IDebugStackFrame2::GetCodeContext](../vs140/IDebugStackFrame2--GetCodeContext.md) to get memory information  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)