---
title: "BP_PASSCOUNT"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 791ac175-b897-4c70-873e-240da7e0ac89
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_PASSCOUNT
Describes the count and conditions upon which a conditional breakpoint is fired.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_PASSCOUNT {   
   DWORD              dwPassCount;  
   BP_PASSCOUNT_STYLE stylePassCount;  
} BP_PASSCOUNT;  
```  
  
```c#  
public struct BP_PASSCOUNT {   
   public uint dwPassCount;  
   public uint stylePassCount;  
};  
```  
  
## Members  
 `dwPassCount`  
 The number of times to pass over the breakpoint before firing it.  
  
 `stylePassCount`  
 A value from the [BP_PASSCOUNT_STYLE](../vs140/BP_PASSCOUNT_STYLE.md) enumeration that specifies the style of the breakpoint pass count.  
  
## Remarks  
 This structure is a member of the [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) structure.  
  
 This structure is also passed as a parameter to the[SetPassCount](../vs140/IDebugBoundBreakpoint2--SetPassCount.md) and[SetPassCount](../vs140/IDebugPendingBreakpoint2--SetPassCount.md) methods.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)   
 [SetPassCount](../vs140/IDebugBoundBreakpoint2--SetPassCount.md)   
 [SetPassCount](../vs140/IDebugPendingBreakpoint2--SetPassCount.md)   
 [BP_PASSCOUNT_STYLE](../vs140/BP_PASSCOUNT_STYLE.md)