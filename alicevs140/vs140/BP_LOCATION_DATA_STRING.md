---
title: "BP_LOCATION_DATA_STRING"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 445d6f3f-95b0-47ac-85e2-51b778240687
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_DATA_STRING
Used for setting data breakpoints that are based on a string that the user can enter from the integrated development environment (IDE).  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION_DATA_STRING {   
   IDebugThread2* pThread;  
   BSTR           bstrContext;  
   BSTR           bstrDataExpr;  
   DWORD          dwNumElements;  
} BP_LOCATION_DATA_STRING;  
```  
  
## Members  
 `pThread`  
 The [IDebugThread2](../vs140/IDebugThread2.md) object that represents the thread on which the breakpoint occurs.  
  
 `bstrContext`  
 The context of the breakpoint within the code, typically a method or function name as seen on a call stack.  
  
 `bstrDataExpr`  
 The data string the user enters to set the breakpoint.  
  
 `dwNumElements`  
 The number of elements in the data string in which the breakpoint occurs.  
  
## Remarks  
 This structure is a member of the [BP_LOCATION](../vs140/BP_LOCATION.md) structure as part of a union.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)