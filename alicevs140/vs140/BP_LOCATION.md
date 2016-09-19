---
title: "BP_LOCATION"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed1e874c-f289-4c31-8b6c-04dde03ad0f5
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION
Specifies the type of structure used to describe the location of the breakpoint.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION {  
   BP_LOCATION_TYPE bpLocationType;  
   union {  
      BP_LOCATION_CODE_FILE_LINE   bplocCodeFileLine;  
      BP_LOCATION_CODE_FUNC_OFFSET bplocCodeFuncOffset;  
      BP_LOCATION_CODE_CONTEXT     bplocCodeContext;  
      BP_LOCATION_CODE_STRING      bplocCodeString;  
      BP_LOCATION_CODE_ADDRESS     bplocCodeAddress;  
      BP_LOCATION_DATA_STRING      bplocDataString;  
      BP_LOCATION_RESOLUTION       bplocResolution;  
      DWORD                        unused;  
   } bpLocation;  
} BP_LOCATION;  
```  
  
```c#  
public struct BP_LOCATION {  
   public uint   bpLocationType;  
   public IntPtr unionmember1;  
   public IntPtr unionmember2;  
   public IntPtr unionmember3;  
   public IntPtr unionmember4;  
};  
```  
  
## Members  
 `bpLocationType`  
 A value from the [BP_LOCATION_TYPE](../vs140/BP_LOCATION_TYPE.md) enumeration used to interpret the `bpLocation` union or the `unionmemberX` members.  
  
 `bpLocation`.`bplocCodeFileLine`  
 [C++ only] Contains the [BP_LOCATION_CODE_FILE_LINE](../vs140/BP_LOCATION_CODE_FILE_LINE.md) structure if `bpLocationType` = `BPLT_CODE_FILE_LINE`.  
  
 `bpLocation.bplocCodeFuncOffset`  
 [C++ only] Contains the [BP_LOCATION_CODE_FUNC_OFFSET](../vs140/BP_LOCATION_CODE_FUNC_OFFSET.md) structure if `bpLocationType` = `BPLT_CODE_FUNC_OFFSET`.  
  
 `bpLocation.bplocCodeContext`  
 [C++ only] Contains the [BP_LOCATION_CODE_CONTEXT](../vs140/BP_LOCATION_CODE_CONTEXT.md) structure if `bpLocationType` = `BPLT_CODE_CONTEXT`.  
  
 `bpLocation.bplocCodeString`  
 [C++ only] Contains the [BP_LOCATION_CODE_STRING](../vs140/BP_LOCATION_CODE_STRING.md) structure if `bpLocationType` = `BPLT_CODE_STRING`.  
  
 `bpLocation.bplocCodeAddress`  
 [C++ only] Contains the [BP_LOCATION_CODE_ADDRESS](../vs140/BP_LOCATION_CODE_ADDRESS.md) structure if `bpLocationType` = `BPLT_CODE_ADDRESS`.  
  
 `bpLocation.bplocDataString`  
 [C++ only] Contains the [BP_LOCATION_DATA_STRING](../vs140/BP_LOCATION_DATA_STRING.md) structure if `bpLocationType` = `BPLT_DATA_STRING`.  
  
 `bpLocation.bplocResolution`  
 [C++ only] Contains the [BP_LOCATION_RESOLUTION](../vs140/BP_LOCATION_RESOLUTION.md) structure if `bpLocationType` = `BPLT_RESOLUTION`.  
  
 `unionmember1`  
 [C# only] See Remarks on how to interpret.  
  
 `unionmember2`  
 [C# only] See Remarks on how to interpret.  
  
 `unionmember3`  
 [C# only] See Remarks on how to interpret.  
  
 `unionmember4`  
 [C# only] See Remarks on how to interpret.  
  
## Remarks  
 This structure is a member of the [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) and [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md) structures.  
  
 [C# only] The `unionmemberX` members are interpreted according to the following table. Look down the left column for the `bpLocationType` value then look across the other columns to determine what each `unionmemberX` member represents and marshal the `unionmemberX` accordingly. See the example for a way to interpret a part of this structure in C#.  
  
|`bpLocationType`|`unionmember1`|`unionmember2`|`unionmember3`|`unionmember4`|  
|----------------------|--------------------|--------------------|--------------------|--------------------|  
|`BPLT_CODE_FILE_LINE`|`string` (a context)|[IDebugDocumentPosition2](../vs140/IDebugDocumentPosition2.md)|-|-|  
|`BPLT_CODE_FUNC_OFFSET`|`string` (a context)|[IDebugFunctionPosition2](../vs140/IDebugFunctionPosition2.md)|-|-|  
|`BPLT_CODE_CONTEXT`|[IDebugCodeContext2](../vs140/IDebugCodeContext2.md)|-|-|-|  
|`BPLT_CODE_STRING`|`string` (a context)|`string` (conditional expression)|-|-|  
|`BPLT_CODE_ADDRESS`|`string` (a context)|`string` (module URL)|`string` (function name)|`string` (address)|  
|`BPLT_DATA_STRING`|[IDebugThread2](../vs140/IDebugThread2.md)|`string` (a context)|`string` (data expression)|`uint` (number of elements)|  
|`BPLT_RESOLUTION`|[IDebugBreakpointResolution2](../vs140/IDebugBreakpointResolution2.md)|-|-|-|  
  
## Example  
 This example shows how to interpret the `BP_LOCATION` structure in C# for the `BPLT_DATA_STRING` type. This particular type shows how to interpret all four `unionmemberX` members in all possible formats (object, string, and number).  
  
```c#  
using System;  
using System.Runtime.Interop.Services;  
using Microsoft.VisualStudio.Debugger.Interop;  
  
namespace MyPackage  
{  
    public class MyClass  
    {  
        public void Interpret(BP_LOCATION bp)  
        {  
            if (bp.bpLocationType == (uint)enum_BP_LOCATION_TYPE.BPLT_DATA_STRING)  
            {  
                 IDebugThread2 pThread = (IDebugThread2)Marshal.GetObjectForIUnknown(bp.unionmember1);  
                 string context = Marshal.PtrToStringBSTR(bp.unionmember2);  
                 string dataExpression = Marshal.PtrToStringBSTR(bp.unionmember3);  
                 uint numElements = (uint)Marshal.ReadInt32(bp.unionmember4);  
            }  
        }  
    }  
}  
```  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)   
 [BP_LOCATION_CODE_FILE_LINE](../vs140/BP_LOCATION_CODE_FILE_LINE.md)   
 [BP_LOCATION_CODE_FUNC_OFFSET](../vs140/BP_LOCATION_CODE_FUNC_OFFSET.md)   
 [BP_LOCATION_CODE_CONTEXT](../vs140/BP_LOCATION_CODE_CONTEXT.md)   
 [BP_LOCATION_CODE_STRING](../vs140/BP_LOCATION_CODE_STRING.md)   
 [BP_LOCATION_CODE_ADDRESS](../vs140/BP_LOCATION_CODE_ADDRESS.md)   
 [BP_LOCATION_DATA_STRING](../vs140/BP_LOCATION_DATA_STRING.md)   
 [BP_LOCATION_RESOLUTION](../vs140/BP_LOCATION_RESOLUTION.md)