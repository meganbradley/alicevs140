---
title: "DEBUGPROP_INFO_FLAGS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c7fe777-615e-4929-9ed4-970d9fe0eb81
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# DEBUGPROP_INFO_FLAGS
Specifies what information to retrieve about a debug property object.  
  
## Syntax  
  
```cpp#  
enum enum_DEBUGPROP_INFO_FLAGS {   
   DEBUGPROP_INFO_FULLNAME          = 0x00000001,  
   DEBUGPROP_INFO_NAME              = 0x00000002,  
   DEBUGPROP_INFO_TYPE              = 0x00000004,  
   DEBUGPROP_INFO_VALUE             = 0x00000008,  
   DEBUGPROP_INFO_ATTRIB            = 0x00000010,  
   DEBUGPROP_INFO_PROP              = 0x00000020,  
   DEBUGPROP_INFO_VALUE_AUTOEXPAND  = 0x00010000,  
   DEBUGPROP_INFO_VALUE_NOFUNCEVAL  = 0x00020000,  
   DEBUGPROP_INFO_VALUE_RAW         = 0x00040000,  
   DEBUGPROP_INFO_VALUE_NO_TOSTRING = 0x00080000  
   DEBUGPROP_INFO_NONE              = 0x00000000,  
   DEBUGPROP_INFO_STANDARD          = DEBUGPROP_INFO_ATTRIB |  
                                      DEBUGPROP_INFO_NAME |  
                                      DEBUGPROP_INFO_TYPE |  
                                      DEBUGPROP_INFO_VALUE,  
   DEBUGPROP_INFO_ALL               = 0xffffffff  
};  
typedef DWORD DEBUGPROP_INFO_FLAGS;  
```  
  
```c#  
public enum enum_DEBUGPROP_INFO_FLAGS {   
   DEBUGPROP_INFO_FULLNAME          = 0x00000001,  
   DEBUGPROP_INFO_NAME              = 0x00000002,  
   DEBUGPROP_INFO_TYPE              = 0x00000004,  
   DEBUGPROP_INFO_VALUE             = 0x00000008,  
   DEBUGPROP_INFO_ATTRIB            = 0x00000010,  
   DEBUGPROP_INFO_PROP              = 0x00000020,  
   DEBUGPROP_INFO_VALUE_AUTOEXPAND  = 0x00010000,  
   DEBUGPROP_INFO_VALUE_NOFUNCEVAL  = 0x00020000,  
   DEBUGPROP_INFO_VALUE_RAW         = 0x00040000,  
   DEBUGPROP_INFO_VALUE_NO_TOSTRING = 0x00080000  
   DEBUGPROP_INFO_NONE              = 0x00000000,  
   DEBUGPROP_INFO_STANDARD          = DEBUGPROP_INFO_ATTRIB |  
                                      DEBUGPROP_INFO_NAME |  
                                      DEBUGPROP_INFO_TYPE |  
                                      DEBUGPROP_INFO_VALUE,  
   DEBUGPROP_INFO_ALL               = 0xffffffff  
};  
```  
  
## Members  
 DEBUGPROP_INFO_FULLNAME  
 Initialize/use the `bstrFullName` field.  
  
 DEBUGPROP_INFO_NAME  
 Initialize/use the `bstrName` field.  
  
 DEBUGPROP_INFO_TYPE  
 Initialize/use the `bstrType` field.  
  
 DEBUGPROP_INFO_VALUE  
 Initialize/use the `bstrValue` field.  
  
 DEBUGPROP_INFO_ATTRIB  
 Initialize/use the `dwAttrib` field.  
  
 DEBUGPROP_INFO_PROP,  
 Initialize/use the `pProperty` field that contains an [IDebugProperty2](../vs140/IDebugProperty2.md) interface.  
  
 DEBUGPROP_INFO_VALUE_AUTOEXPAND  
 Specifies that the value field should contain the auto-expanded value, if available, for this type of object.  
  
 DEBUGPROP_INFO_VALUE_NOFUNCEVAL  
 Deprecated.  
  
 DEBUGPROP_INFO_VALUE_RAW  
 Do not return any beautified values or members (that is, do not format the values).  
  
 DEBUGPROP_INFO_VALUE_NO_TOSTRING  
 Do not return any special synthesized values (for example, do not call `ToString()` on an object to produce a value).  
  
 DEBUGPROP_INFO_NONE  
 Specifies that no flags are set.  
  
 DEBUGPROP_INFO_STANDARD  
 Initialize/use the `dwAttrib`, `bstrName`, `bstrType`, and `bstrValue` fields.  
  
 DEBUGPROP_INFO_All  
 Indicates a mask of all flags.  
  
## Remarks  
 These values are passed to the [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md), [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md), and [IDebugStackFrame2::EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md) methods to indicate which fields are to be initialized the [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structure.  
  
 These values are also used for the `dwFields` member of the `DEBUG_PROPERTY_INFO` structure to indicate which fields of the structure are used and valid when the structure is returned.  
  
 These values may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md)   
 [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md)   
 [IDebugStackFrame2::EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md)   
 [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md)