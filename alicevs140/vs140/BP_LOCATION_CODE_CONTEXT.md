---
title: "BP_LOCATION_CODE_CONTEXT"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37412896-021a-4f73-9bb7-4125502c2e18
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_CODE_CONTEXT
Describes the location of a breakpoint that is bound directly to an address in the program being debugged.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION_CODE_CONTEXT {   
   IDebugCodeContext2* pCodeContext;  
} BP_LOCATION_CODE_CONTEXT;  
```  
  
## Members  
 pCodeContext  
 The [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object that identifies the position of the breakpoint in the code.  
  
## Remarks  
 This structure is a member of the [BP_LOCATION](../vs140/BP_LOCATION.md) structure as part of a union.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)