---
title: "CONTEXT_INFO_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef436bd3-738e-47e8-828c-8febce752439
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# CONTEXT_INFO_FIELDS
Specifies what information to retrieve about a memory context.  
  
## Syntax  
  
```cpp#  
enum enum_CONTEXT_INFO_FIELDS {   
   CIF_MODULEURL =       0x00000001,  
   CIF_FUNCTION =        0x00000002,  
   CIF_FUNCTIONOFFSET =  0x00000004,  
   CIF_ADDRESS =         0x00000008,  
   CIF_ADDRESSOFFSET =   0x00000010,  
   CIF_ADDRESSABSOLUTE = 0x00000020,  
   CIF_ALLFIELDS =       0x0000003f  
};  
typedef DWORD CONTEXT_INFO_FIELDS;  
```  
  
```c#  
public enum enum_CONTEXT_INFO_FIELDS {  
   CIF_MODULEURL =       0x00000001,  
   CIF_FUNCTION =        0x00000002,  
   CIF_FUNCTIONOFFSET =  0x00000004,  
   CIF_ADDRESS =         0x00000008,  
   CIF_ADDRESSOFFSET =   0x00000010,  
   CIF_ADDRESSABSOLUTE = 0x00000020,  
   CIF_ALLFIELDS =       0x0000003f  
};  
```  
  
## Members  
 CIF_MODULEURL  
 Initialize/use the `bstrModuleUrl` field of the [CONTEXT_INFO](../vs140/CONTEXT_INFO.md) structure.  
  
 CIF_FUNCTION  
 Initialize/use the `bstrFunction` field of the `CONTEXT_INFO` structure.  
  
 CIF_FUNCTIONOFFSET  
 Initialize/use the `posFunctionOffset` field of the `CONTEXT_INFO` structure.  
  
 CIF_ADDRESS  
 Initialize/use the `bstrAddress` field of the `CONTEXT_INFO` structure.  
  
 CIF_ADDRESSOFFSET  
 Initialize/use the `bstrAddressOffset` field of the `CONTEXT_INFO` structure.  
  
 CIF_ALLFIELDS  
 Initialize/use all fields of the `CONTEXT_INFO` structure.  
  
## Remarks  
 These values are passed a parameter to the [GetInfo](../vs140/IDebugMemoryContext2--GetInfo.md) method to indicate which fields of the [CONTEXT_INFO](../vs140/CONTEXT_INFO.md) structure are to be initialized.  
  
 These flags are also used to indicate which fields of the `CONTEXT_INFO` structure are used and valid when the structure is returned.  
  
 These values may be combined with a bitwise OR.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [CONTEXT_INFO](../vs140/CONTEXT_INFO.md)   
 [GetInfo](../vs140/IDebugMemoryContext2--GetInfo.md)