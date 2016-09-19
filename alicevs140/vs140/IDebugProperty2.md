---
title: "IDebugProperty2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7d5c70f-a1a5-4120-9f70-184e01c25bff
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProperty2
This interface represents a stack frame property, a program document property, or some other property. The property is usually the result of an expression evaluation.  
  
> [!NOTE]
>  This use of "property" should not be confused with that meaning a member variable of a class, although an `IDebugProperty2` can represent such an entity.  
  
## Syntax  
  
```  
IDebugProperty2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to represent a particular kind of value. For example, the value could be a numerical value as a result of an expression evaluation, a memory context used for displaying memory, or a list of registers and their values.  
  
## Notes for Callers  
 Call [IDebugExpression2::EvaluateSync](../vs140/IDebugExpression2--EvaluateSync.md) or [IDebugExpression2::EvaluateAsync](../vs140/IDebugExpression2--EvaluateAsync.md) to obtain this interface, which represents the result of an evaluation. `IDebugExpression2::EvaluateAsync` returns this interface by sending an [IDebugExpressionEvaluationCompleteEvent2](../vs140/IDebugExpressionEvaluationCompleteEvent2.md) interface to the SDM, which in turn calls [IDebugExpressionEvaluationCompleteEvent2::GetResult](../vs140/IDebugExpressionEvaluationCompleteEvent2--GetResult.md) to retrieve the property.  
  
 [IDebugPropertyCreateEvent2::GetDebugProperty](../vs140/IDebugPropertyCreateEvent2--GetDebugProperty.md) returns this interface to provide the associated script document.  
  
 [IDebugReturnValueEvent2::GetReturnValue](../vs140/IDebugReturnValueEvent2--GetReturnValue.md) returns this interface to represent the return value of a function.  
  
 [IDebugProgram2::GetDebugProperty](../vs140/IDebugProgram2--GetDebugProperty.md) returns this interface to represent various properties of the program such as a name or a memory context.  
  
 [IDebugStackFrame2::GetDebugProperty](../vs140/IDebugStackFrame2--GetDebugProperty.md) returns this interface to represent various properties of the stack frame such as local variables.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProperty2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md)|Fills in a [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structure that describes a property.|  
|[SetValueAsString](../vs140/IDebugProperty2--SetValueAsString.md)|Sets the value of a property from a string.|  
|[IDebugProperty2::SetValueAsReference](../vs140/IDebugProperty2--SetValueAsReference.md)|Sets the value of the property from the value of a given reference.|  
|[EnumChildren](../vs140/IDebugProperty2--EnumChildren.md)|Enumerates the children of a property.|  
|[GetParent](../vs140/IDebugProperty2--GetParent.md)|Returns the parent of a property.|  
|[GetDerivedMostProperty](../vs140/IDebugProperty2--GetDerivedMostProperty.md)|Returns the property that describes the most-derived property of a property.|  
|[GetMemoryBytes](../vs140/IDebugProperty2--GetMemoryBytes.md)|Returns the memory bytes that compose the value of a property.|  
|[GetMemoryContext](../vs140/IDebugProperty2--GetMemoryContext.md)|Returns the memory context for a property value.|  
|[GetSize](../vs140/IDebugProperty2--GetSize.md)|Returns the size, in bytes, of the property value.|  
|[IDebugProperty2::GetReference](../vs140/IDebugProperty2--GetReference.md)|Returns a reference to this property's value.|  
|[GetExtendedInfo](../vs140/IDebugProperty2--GetExtendedInfo.md)|Returns the extended information of a property.|  
  
## Remarks  
 A property, as represented by an `IDebugProperty2` interface, can be thought of as a value with a name, a type, and an address. In more general terms, an `IDebugProperty2` can represent anything that has a hierarchical structure, with parents and child nodes.  
  
 A property is usually transitory, lasting only as long as the current stack frame, for example. On the other hand, a reference, as represented by an [IDebugReference2](../vs140/IDebugReference2.md) interface, lasts as long as the value remains in memory.  
  
 The IDE can use the `IDebugProperty2` interface to let users browse and modify properties at run time.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md)   
 [IDebugReference2](../vs140/IDebugReference2.md)