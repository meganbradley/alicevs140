---
title: "BP_PASSCOUNT_STYLE"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0a647047-e2d5-4724-a0b8-68108425ecad
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_PASSCOUNT_STYLE
Specifies the condition associated with the breakpoint pass count that causes the breakpoint to fire.  
  
## Syntax  
  
```cpp#  
enum enum_BP_PASSCOUNT_STYLE {   
   BP_PASSCOUNT_NONE             = 0x0000,  
   BP_PASSCOUNT_EQUAL            = 0x0001,  
   BP_PASSCOUNT_EQUAL_OR_GREATER = 0x0002,  
   BP_PASSCOUNT_MOD              = 0x0003  
};  
typedef DWORD BP_PASSCOUNT_STYLE;  
```  
  
```c#  
public enum enum_BP_PASSCOUNT_STYLE {   
   BP_PASSCOUNT_NONE             = 0x0000,  
   BP_PASSCOUNT_EQUAL            = 0x0001,  
   BP_PASSCOUNT_EQUAL_OR_GREATER = 0x0002,  
   BP_PASSCOUNT_MOD              = 0x0003  
};  
```  
  
## Members  
 BP_PASSCOUNT_NONE  
 Specifies no breakpoint pass count style.  
  
 BP_PASSCOUNT_EQUAL  
 Sets the breakpoint pass count style to equal. The breakpoint fires when the number of times the breakpoint is hit equals the pass count.  
  
 BP_PASSCOUNT_EQUAL_OR_GREATER  
 Sets the breakpoint pass count style to equal or greater. The breakpoint fires when the number of times the breakpoint is hit is equal to or greater than the pass count.  
  
 BP_PASSCOUNT_MOD  
 Specifies a modulo pass count. For example, if the pass count is of the type `BP_PASSCOUNT_MOD` and the pass count value is 4, the breakpoint fires every time the hit count is a multiple of 4.  
  
## Remarks  
 Used for the `stylePassCount` member of the [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md) structure that is in turn a member of the [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) and [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md) structures.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [BP_PASSCOUNT](../vs140/BP_PASSCOUNT.md)   
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)   
 [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md)