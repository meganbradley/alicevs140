---
title: "IEnumDebugPropertyInfo2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdea8262-40b8-473e-88ba-639e4c4648e6
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugPropertyInfo2
This interface enumerates [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures.  
  
## Syntax  
  
```  
IEnumDebugPropertyInfo2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent information for a particular property.  
  
## Notes for Callers  
 Call [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md) to obtain this interface representing the children of a particular property. Call [IDebugStackFrame2::EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md) to obtain this interface representing the properties of a particular stack frame.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugPropertyInfo2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugPropertyInfo2--Next.md)|Retrieves a specified number of [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugPropertyInfo2--Skip.md)|Skips a specified number of [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugPropertyInfo2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugPropertyInfo2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugPropertyInfo2--GetCount.md)|Gets the number of [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures in an enumerator.|  
  
## Remarks  
 In general, a property is a hierarchy of information that can include a name, value, address, and type, as well as any other information appropriate to the associated property object or stack frame. See [IDebugProperty2](../vs140/IDebugProperty2.md) for more details.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md)   
 [IDebugStackFrame2::EnumProperties](../vs140/IDebugStackFrame2--EnumProperties.md)