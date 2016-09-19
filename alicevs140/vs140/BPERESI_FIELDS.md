---
title: "BPERESI_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dd7dd89c-1043-46a1-a929-099cc039c344
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BPERESI_FIELDS
Specifies the information to be retrieved about a failed resolution of a breakpoint.  
  
## Syntax  
  
```cpp#  
enum enum_BPERESI_FIELDS {   
   PERESI_BPRESLOCATION = 0x0001,  
   BPERESI_PROGRAM      = 0x0002,  
   BPERESI_THREAD       = 0x0004,  
   BPERESI_MESSAGE      = 0x0008,  
   BPERESI_TYPE         = 0x0010,  
   BPERESI_ALLFIELDS    = 0xffffffff  
};  
typedef DWORD BPERESI_FIELDS;  
```  
  
```c#  
public enum enum_BPERESI_FIELDS {   
   PERESI_BPRESLOCATION = 0x0001,  
   BPERESI_PROGRAM      = 0x0002,  
   BPERESI_THREAD       = 0x0004,  
   BPERESI_MESSAGE      = 0x0008,  
   BPERESI_TYPE         = 0x0010,  
   BPERESI_ALLFIELDS    = 0xffffffff  
};  
```  
  
## Members  
 PERESI_BPRESLOCATION  
 Initialize/use the `bpResLocation` (breakpoint resolution location) field of the [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md) structure.  
  
 BPERESI_PROGRAM  
 Initialize/use the `pProgram` field of the `BP_ERROR_RESOLUTION_INFO` structure.  
  
 BPERESI_THREAD  
 Initialize/use the `pThread` field of the `BP_ERROR_RESOLUTION_INFO` structure.  
  
 BPERESI_MESSAGE  
 Initialize/use the `bstrMessage` field of the `BP_ERROR_RESOLUTION_INFO` structure.  
  
 BPERESI_TYPE  
 Initialize/use the `dwType` (breakpoint type) field of the `BP_ERROR_RESOLUTION_INFO` structure.  
  
 BPERESI_ALLFIELDS  
 Initialize/use all fields of the `BP_ERROR_RESOLUTION_INFO` structure.  
  
## Remarks  
 Passed as a parameter to the [GetResolutionInfo](../vs140/IDebugErrorBreakpointResolution2--GetResolutionInfo.md) method to indicate which fields of the [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md) structure are to be initialized.  
  
 These values are also used to indicate which fields in the `BP_ERROR_RESOLUTION_INFO` structure are used and valid when that structure is returned.  
  
 These values may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md)   
 [GetResolutionInfo](../vs140/IDebugErrorBreakpointResolution2--GetResolutionInfo.md)