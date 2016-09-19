---
title: "BP_LOCATION_CODE_FUNC_OFFSET"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab38f7ca-fa01-4cf3-a06c-56cbb7207617
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_CODE_FUNC_OFFSET
Describes the offset location of a breakpoint in a function in code.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION_CODE_FUNC_OFFSET {   
   BSTR                     bstrContext;  
   IDebugFunctionPosition2* pFuncPos;  
} BP_LOCATION_CODE_FUNC_OFFSET;  
```  
  
## Members  
 `bstrContext`  
 The context of the breakpoint, typically a method or function name as seen on a call stack.  
  
 `pFuncPos`  
 The [IDebugFunctionPosition2](../vs140/IDebugFunctionPosition2.md) object that describes the name of the function and the relative position from the beginning of the function.  
  
## Remarks  
 This structure is a member of the [BP_LOCATION](../vs140/BP_LOCATION.md) structure as part of a union.  
  
 The `pFuncPos` member indicates where to set the function breakpoint.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)   
 [IDebugFunctionPosition2](../vs140/IDebugFunctionPosition2.md)