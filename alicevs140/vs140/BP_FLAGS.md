---
title: "BP_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c45dfc74-5e7f-4f1e-a147-ab2a55dccbd0
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_FLAGS
Provides optional flags that may be used to specify additional information when setting a breakpoint.  
  
## Syntax  
  
```cpp#  
enum enum_BP_FLAGS {   
   BP_FLAG_NONE            = 0x0000,  
   BP_FLAG_MAP_DOCPOSITION = 0x0001,  
   BP_FLAG_DONT_STOP       = 0x0002  
};  
typedef DWORD BP_FLAGS;  
```  
  
```c#  
public enum enum_BP_FLAGS {   
   BP_FLAG_NONE            = 0x0000,  
   BP_FLAG_MAP_DOCPOSITION = 0x0001,  
   BP_FLAG_DONT_STOP       = 0x0002  
};  
```  
  
## Members  
 BP_FLAG_NONE  
 Specifies no breakpoint flag.  
  
 BP_FLAG_MAP_DOCPOSITION  
 Specifies that the debug engine (DE) should map the breakpoint using the document position. This is applicable only to breakpoints set in script-oriented source files such as Active Server Pages (ASP).  
  
 BP_FLAG_DONT_STOP  
 Specifies that the breakpoint should be processed by the debug engine, but that the debug engine ultimately should not stop there (that is, an [IDebugBreakpointEvent2](../vs140/IDebugBreakpointEvent2.md) event object should not be sent). This flag is designed to be used primarily with tracepoints.  
  
## Remarks  
 Used for the `dwFlags` member of the [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) and [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md) structures.  
  
 These values may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)   
 [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md)   
 [IDebugBreakpointEvent2](../vs140/IDebugBreakpointEvent2.md)