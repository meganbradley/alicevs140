---
title: "BP_RESOLUTION_DATA"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e0b9000-6a84-47b9-b07a-367a75764389
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_RESOLUTION_DATA
Describes the result of binding a data breakpoint.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_RESOLUTION_DATA {   
   BSTR              bstrDataExpr;  
   BSTR              bstrFunc;  
   BSTR              bstrImage;  
   BP_RES_DATA_FLAGS dwFlags;  
} BP_RESOLUTION_DATA;  
```  
  
```c#  
public struct BP_RESOLUTION_DATA {   
   public string bstrDataExpr;  
   public string bstrFunc;  
   public string bstrImage;  
   public uint   dwFlags;  
};  
```  
  
## Members  
 `bstrDataExpr`  
 The data expression that has been bound.  
  
 `bstrFunc`  
 The name of the function the data breakpoint has bound in (if any).  
  
 `bstrImage`  
 The name of the module (MyModule.dll, for example) that the data breakpoint has bound in.  
  
 `dwFlags`  
 A value from the [BP_RES_DATA_FLAGS](../vs140/BP_RES_DATA_FLAGS.md) enumeration, describing how the data breakpoint is implemented.  
  
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