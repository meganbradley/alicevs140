---
title: "BP_UNBOUND_REASON"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 939b6f9c-113b-471d-9f30-b03871af6285
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_UNBOUND_REASON
Gives the reason a breakpoint was unbound.  
  
## Syntax  
  
```cpp#  
enum enum_BP_UNBOUND_REASON {   
   BPUR_UNKNOWN           = 0x0000,  
   BPUR_CODE_UNLOADED     = 0x0002,  
   BPUR_BREAKPOINT_REBIND = 0x0003,  
   BPUR_BREAKPOINT_ERROR  = 0x0004  
};  
typedef DWORD BP_UNBOUND_REASON;  
```  
  
```c#  
public enum enum_BP_UNBOUND_REASON {   
   BPUR_UNKNOWN           = 0x0000,  
   BPUR_CODE_UNLOADED     = 0x0002,  
   BPUR_BREAKPOINT_REBIND = 0x0003,  
   BPUR_BREAKPOINT_ERROR  = 0x0004  
};  
```  
  
## Members  
 BPUR_UNKNOWN  
 The reason is unknown.  
  
 BPUR_CODE_UNLOADED  
 The code that contains the breakpoint has been unloaded.  
  
 BPUR_BREAKPOINT_REBIND  
 The breakpoint has been rebound to a different location. This can happen after Edit and Continue operations when the breakpoint moves, or when the breakpoint is bound to a file with a path that is no longer valid.  
  
 BPUR_ BREAKPOINT_ERROR  
 The breakpoint is determined to be in error after it is bound. This happens to managed breakpoints whose conditions are no longer valid.  
  
## Remarks  
 Returned by the [GetReason](../vs140/IDebugBreakpointUnboundEvent2--GetReason.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [GetReason](../vs140/IDebugBreakpointUnboundEvent2--GetReason.md)