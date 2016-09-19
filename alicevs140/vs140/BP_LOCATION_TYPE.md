---
title: "BP_LOCATION_TYPE"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0248430a-3b61-4809-87a9-e9b6bb7d1130
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_TYPE
Specifies the location type of the breakpoint for a breakpoint request.  
  
## Syntax  
  
```cpp#  
enum enum_BP_LOCATION_TYPE {   
   BPLT_NONE               = 0x00000000,  
   BPLT_FILE_LINE          = 0x00010000,  
   BPLT_FUNC_OFFSET        = 0x00020000,  
   BPLT_CONTEXT            = 0x00030000,  
   BPLT_STRING             = 0x00040000,  
   BPLT_ADDRESS            = 0x00050000,  
   BPLT_RESOLUTION         = 0x00060000,  
   BPLT_CODE_FILE_LINE     = BPT_CODE | BPLT_FILE_LINE,  
   BPLT_CODE_FUNC_OFFSET   = BPT_CODE | BPLT_FUNC_OFFSET,  
   BPLT_CODE_CONTEXT       = BPT_CODE | BPLT_CONTEXT,  
   BPLT_CODE_STRING        = BPT_CODE | BPLT_STRING,  
   BPLT_CODE_ADDRESS       = BPT_CODE | BPLT_ADDRESS ,  
   BPLT_DATA_STRING        = BPT_DATA | BPLT_STRING,  
   BPLT_TYPE_MASK          = 0x0000FFFF,  
   BPLT_LOCATION_TYPE_MASK = 0xFFFF0000  
};  
typedef DWORD BP_LOCATION_TYPE;  
```  
  
```c#  
public enum enum_BP_LOCATION_TYPE {   
   BPLT_NONE               = 0x00000000,  
   BPLT_FILE_LINE          = 0x00010000,  
   BPLT_FUNC_OFFSET        = 0x00020000,  
   BPLT_CONTEXT            = 0x00030000,  
   BPLT_STRING             = 0x00040000,  
   BPLT_ADDRESS            = 0x00050000,  
   BPLT_RESOLUTION         = 0x00060000,  
   BPLT_CODE_FILE_LINE     = BPT_CODE | BPLT_FILE_LINE,  
   BPLT_CODE_FUNC_OFFSET   = BPT_CODE | BPLT_FUNC_OFFSET,  
   BPLT_CODE_CONTEXT       = BPT_CODE | BPLT_CONTEXT,  
   BPLT_CODE_STRING        = BPT_CODE | BPLT_STRING,  
   BPLT_CODE_ADDRESS       = BPT_CODE | BPLT_ADDRESS ,  
   BPLT_DATA_STRING        = BPT_DATA | BPLT_STRING,  
   BPLT_TYPE_MASK          = 0x0000FFFF,  
   BPLT_LOCATION_TYPE_MASK = 0xFFFF0000  
};  
```  
  
## Members  
 BPLT_NONE  
 Specifies no breakpoint location.  
  
 BPLT_FILE_LINE  
 Specifies the location type of the breakpoint as a file line.  
  
 BPLT_FUNC_OFFSET  
 Specifies the location type of the breakpoint as a function offset.  
  
 BPLT_CONTEXT  
 Specifies the location type of the breakpoint as a context.  
  
 BPLT_STRING  
 Specifies the location type of the breakpoint as a string.  
  
 BPLT_ADDRESS  
 Specifies the location type of the breakpoint as an address.  
  
 BPLT_RESOLUTION  
 Specifies the location type of the breakpoint as a resolution.  
  
 BPLT_CODE_FILE_LINE  
 Specifies the location type of the breakpoint as a line of source code.  
  
 BPLT_CODE_FUNC_OFFSET  
 Specifies the location type of the breakpoint as a code function offset.  
  
 BPLT_CODE_CONTEXT  
 Specifies the location type of the breakpoint as a code context.  
  
 BPLT_CODE_STRING  
 Specifies the location type of the breakpoint as a code string.  
  
 BPLT_CODE_ADDRESS  
 Specifies the location type of the breakpoint as a code address.  
  
 BPLT_DATA_STRING  
 Specifies the location type of the breakpoint as a data string.  
  
 BPLT_TYPE_MASK  
 Specifies a bit mask, so that the breakpoint type can be extracted out of the value.  
  
 BPLT_LOCATION_TYPE_MASK  
 Specifies a bit mask, so that the breakpoint location type can be extracted out of the value.  
  
## Remarks  
 Passed as a parameter to the [GetLocationType](../vs140/IDebugBreakpointRequest2--GetLocationType.md) method.  
  
 A breakpoint location type is composed of a breakpoint type and a location type. This means that a breakpoint location type is never just a breakpoint type (for example, `BPT_CODE`) or a location type (for example, `BPLT_FILE_LINE`). Predefined constants for all breakpoint location types currently supported are included in this enumeration (`BPLT_CODE_FILE_LINE` through `BPLT_DATA_STRING`).  
  
 `BPT_CODE` and `BPT_DATA` are members of the [BP_TYPE](../vs140/BP_TYPE.md) enumeration.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [GetLocationType](../vs140/IDebugBreakpointRequest2--GetLocationType.md)   
 [BP_TYPE](../vs140/BP_TYPE.md)