---
title: "IDebugStackFrame2::EnumProperties"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 334bb95e-c7e0-4008-9f06-8c3999e47ee8
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStackFrame2::EnumProperties
Creates an enumerator for properties associated with the stack frame, such as local variables.  
  
## Syntax  
  
```cpp#  
HRESULT EnumProperties (   
   DEBUGPROP_INFO_FLAGS      dwFieldSpec,  
   UINT                      nRadix,  
   REFIID                    refiid,  
   DWORD                     dwTimeout,  
   ULONG*                    pcelt,  
   IEnumDebugPropertyInfo2** ppEnum  
);  
```  
  
```c#  
int EnumProperties (   
   enum_DEBUGPROP_INFO_FLAGS   dwFieldSpec,  
   uint                        nRadix,  
   ref Guid                    refiid,  
   uint                        dwTimeout,  
   out uint                    pcelt,  
   out IEnumDebugPropertyInfo2 ppEnum  
);  
```  
  
#### Parameters  
 `dwFieldSpec`  
 [in] A combination of flags from the [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md) enumeration that specifies which fields in the enumerated [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures are to be filled in.  
  
 `nRadix`  
 [in] The radix to be used in formatting any numerical information.  
  
 `refiid`  
 [in] A GUID of a filter used to select which [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures are to be enumerated, such as `guidFilterLocals`.  
  
 `dwTimeout`  
 [in] Maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
 `pcelt`  
 [out] Returns the number of properties enumerated. This is the same as calling the [GetCount](../vs140/IEnumDebugPropertyInfo2--GetCount.md) method.  
  
 `ppEnum`  
 [out] Returns an [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md) object containing a list of the desired properties.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Because this method allows all selected properties to be retrieved with a single call, it is faster than sequentially calling the [IDebugStackFrame2::GetDebugProperty](../vs140/IDebugStackFrame2--GetDebugProperty.md) and [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md) methods.  
  
## See Also  
 [IDebugStackFrame2](../vs140/IDebugStackFrame2.md)   
 [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md)   
 [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md)   
 [GetCount](../vs140/IEnumDebugPropertyInfo2--GetCount.md)   
 [IDebugStackFrame2::GetDebugProperty](../vs140/IDebugStackFrame2--GetDebugProperty.md)   
 [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md)