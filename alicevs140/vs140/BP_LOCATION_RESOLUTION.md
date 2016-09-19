---
title: "BP_LOCATION_RESOLUTION"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86ea2c8a-54a3-48e8-83c7-18a515273129
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_RESOLUTION
Describes the resolution of a breakpoint at a specific location.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION_RESOLUTION {   
   IDebugBreakpointResolution2* pResolution;  
} BP_LOCATION_RESOLUTION;  
```  
  
## Members  
 pResolution  
 The [IDebugBreakpointResolution2](../vs140/IDebugBreakpointResolution2.md) object that determines the type of the breakpoint and its resolution information.  
  
## Remarks  
 This structure is a member of the [BP_LOCATION](../vs140/BP_LOCATION.md) structure as part of a union.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)   
 [IDebugBreakpointResolution2](../vs140/IDebugBreakpointResolution2.md)