---
title: "BP_STATE"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 08aa6a3f-3e5f-4c83-8eca-7b7b5f8e208d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_STATE
Specifies the existence of a bound breakpoint and also specifies if it is enabled.  
  
## Syntax  
  
```cpp#  
enum enum_BP_STATE {   
   BPS_NONE     = 0x0000,  
   BPS_DELETED  = 0x0001,  
   BPS_DISABLED = 0x0002,  
   BPS_ENABLED  = 0x0003  
};  
typedef DWORD BP_STATE;  
```  
  
```c#  
public enum enum_BP_STATE {   
   BPS_NONE     = 0x0000,  
   BPS_DELETED  = 0x0001,  
   BPS_DISABLED = 0x0002,  
   BPS_ENABLED  = 0x0003  
};  
```  
  
## Members  
 BPS_NONE  
 Specifies that no breakpoint exists.  
  
 BPS_DELETED  
 Specifies that the breakpoint has been deleted.  
  
 BPS_DISABLED  
 Specifies that the breakpoint is disabled.  
  
 BPS_ENABLED  
 Specifies that the breakpoint is enabled.  
  
## Remarks  
 Returned from the [GetState](../vs140/IDebugBoundBreakpoint2--GetState.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [GetState](../vs140/IDebugBoundBreakpoint2--GetState.md)