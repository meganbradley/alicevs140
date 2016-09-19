---
title: "BP_LOCATION_CODE_ADDRESS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 83c9da8b-19d9-4be5-b225-854543654901
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_CODE_ADDRESS
Describes the location of a breakpoint at an address in code.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION_CODE_ADDRESS {   
   BSTR bstrContext;  
   BSTR bstrModuleUrl;  
   BSTR bstrFunction;  
   BSTR bstrAddress;  
} BP_LOCATION_CODE_ADDRESS;  
```  
  
## Members  
 `bstrContext`  
 The context of the breakpoint, typically a method or function name as seen on a call stack.  
  
 `bstrModuleUrl`  
 The URL of the module that contains the breakpoint.  
  
 `bstrFunction`  
 The name of the function that contains the breakpoint.  
  
 `bstrAddress`  
 The address of the breakpoint, which is parsed by an expression evaluator to bind it to an [IDebugAddress](../vs140/IDebugAddress.md) object.  
  
## Remarks  
 This structure is a member of the [BP_LOCATION](../vs140/BP_LOCATION.md) structure as part of a union.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)   
 [IDebugAddress](../vs140/IDebugAddress.md)