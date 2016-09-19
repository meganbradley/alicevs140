---
title: "DEBUG_PROPERTY_INFO"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a085d18-62c6-4740-b9e9-3f5db6bfdf7f
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# DEBUG_PROPERTY_INFO
Contains information about a debug property.  
  
## Syntax  
  
```cpp#  
typedef struct tagDEBUG_PROPERTY_INFO {   
   DEBUGPROP_INFO_FLAGS dwValidFields;  
   BSTR                 bstrFullName;  
   BSTR                 bstrName;  
   BSTR                 bstrType;  
   BSTR                 bstrValue;  
   IDebugProperty2*     pProperty;  
   DBG_ATTRIB_FLAGS     dwAttrib;  
} DEBUG_PROPERTY_INFO;  
```  
  
```c#  
public struct DEBUG_PROPERTY_INFO {   
   public uint            dwValidFields;  
   public string          bstrFullName;  
   public string          bstrName;  
   public string          bstrType;  
   public string          bstrValue;  
   public IDebugProperty2 pProperty;  
   public ulong           dwAttrib;  
};  
```  
  
## Members  
 dwValidFields  
 A combination of flags from the [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md) enumeration that specifies which fields are filled in.  
  
 bstrFullName  
 The full name of the property.  
  
 bstrName  
 The property name within a context.  
  
 bstrType  
 The property type as a formatted string.  
  
 bstrValue  
 The property value as a formatted string.  
  
 pProperty  
 The [IDebugProperty2](../vs140/IDebugProperty2.md) object described by this structure.  
  
 dwAttrib  
 A combination of flags from the [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md) enumeration describing the attributes of this property.  
  
## Remarks  
 A property is an object of a hierarchical nature that has a name, type, and value. For example, a property can describe local variables, parameters, watch variables and expressions, and registers.  
  
 This structure is passed to the [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md) method where it is filled in. This structure is also returned as part of a list of this structure from the [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md) interface which, in turn, is returned from a call to the [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md) and [IDebugStackFrame2::EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md) methods.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md)   
 [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md)   
 [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md)   
 [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md)   
 [IDebugStackFrame2::EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md)