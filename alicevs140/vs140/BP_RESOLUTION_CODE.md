---
title: "BP_RESOLUTION_CODE"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ac103ec5-771c-4667-92de-b5abb53bbb52
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_RESOLUTION_CODE
Describes the location of a code breakpoint.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_RESOLUTION_CODE {   
   IDebugCodeContext2* pCodeContext;  
} BP_RESOLUTION_CODE;  
```  
  
```c#  
public struct BP_RESOLUTION_CODE {   
   public IDebugCodeContext2 pCodeContext;  
};  
```  
  
## Members  
 `pCodeContext`  
 The [IDebugCodeContext2](../vs140/IDebugCodeContext2.md) object that identifies the position of the breakpoint in the code.  
  
## Remarks  
 This structure is a member of the [BP_RESOLUTION_LOCATION](../vs140/BP_RESOLUTION_LOCATION.md) structure, which is in turn a member of the [BP_RESOLUTION_INFO](../vs140/BP_RESOLUTION_INFO.md) structure returned by the [GetResolutionInfo](../vs140/IDebugBreakpointResolution2--GetResolutionInfo.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_RESOLUTION_LOCATION](../vs140/BP_RESOLUTION_LOCATION.md)   
 [BP_RESOLUTION_INFO](../vs140/BP_RESOLUTION_INFO.md)   
 [GetResolutionInfo](../vs140/IDebugBreakpointResolution2--GetResolutionInfo.md)   
 [IDebugCodeContext2](../vs140/IDebugCodeContext2.md)