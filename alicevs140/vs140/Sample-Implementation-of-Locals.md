---
title: "Sample Implementation of Locals"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 66a2e00a-f558-4e87-96b8-5ecf5509e04c
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Sample Implementation of Locals
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Here is an overview of how Visual Studio obtains the locals for a method from the expression evaluator (EE):  
  
1.  Visual Studio calls the debug engine's (DE) [IDebugStackFrame2::GetDebugProperty](../vs140/IDebugStackFrame2--GetDebugProperty.md) to get an [IDebugProperty2](../vs140/IDebugProperty2.md) object that represents all the properties of the stack frame, including the locals.  
  
2.  `IDebugStackFrame2::GetDebugProperty` calls [IDebugExpressionEvaluator::GetMethodProperty](../vs140/IDebugExpressionEvaluator--GetMethodProperty.md) to obtain an object that describes the method within which the breakpoint occurred. The DE supplies a symbol provider ([IDebugSymbolProvider](../vs140/IDebugSymbolProvider.md)), an address ([IDebugAddress](../vs140/IDebugAddress.md)), and a binder ([IDebugBinder](../vs140/IDebugBinder.md)).  
  
3.  `IDebugExpressionEvaluator::GetMethodProperty` calls [IDebugSymbolProvider::GetContainerField](../vs140/IDebugSymbolProvider--GetContainerField.md) with the supplied `IDebugAddress` object to get an [IDebugContainerField](../vs140/IDebugContainerField.md) representing the method containing the specified address.  
  
4.  The `IDebugContainerField` interface is queried for the [IDebugMethodField](../vs140/IDebugMethodField.md) interface. It is this interface that gives access to the method's locals.  
  
5.  `IDebugExpressionEvaluator::GetMethodProperty` instantiates a class (called `CFieldProperty` in the sample) that implements the `IDebugProperty2` interface to represent the method's locals. The `IDebugMethodField` object is placed in this `CFieldProperty` object along with the `IDebugSymbolProvider`, `IDebugAddress` and `IDebugBinder` objects.  
  
6.  When the `CFieldProperty` object is initialized, [IDebugField::GetInfo](../vs140/IDebugField--GetInfo.md) is called on the `IDebugMethodField` object to obtain a [FIELD_INFO](../vs140/FIELD_INFO.md) structure that contains all displayable information about the method itself.  
  
7.  `IDebugExpressionEvaluator::GetMethodProperty` returns the `CFieldProperty` object as an `IDebugProperty2` object.  
  
8.  Visual Studio calls [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md) on the returned `IDebugProperty2` object with the filter `guidFilterLocalsPlusArgs`. This returns an [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md) object containing the method's locals. This enumeration is filled in by calls to [IDebugMethodField::EnumLocals](../vs140/IDebugMethodField--EnumLocals.md) and [IDebugMethodField::EnumArguments](../vs140/IDebugMethodField--EnumArguments.md).  
  
9. Visual Studio calls [IEnumDebugPropertyInfo2::Next](../vs140/IEnumDebugPropertyInfo2--Next.md) to obtain a [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structure for each local. This structure contains a pointer to an `IDebugProperty2` interface for a local.  
  
10. Visual Studio calls [IDebugProperty2::GetPropertyInfo](../vs140/IDebugProperty2--GetPropertyInfo.md) for each local to obtain the local's name, value, and type. This is the information that is displayed in the **Locals** window.  
  
## In This Section  
 [Implementing GetMethodProperty](../vs140/Implementing-GetMethodProperty.md)  
 Describes an implementation of [IDebugExpressionEvaluator::GetMethodProperty](../vs140/IDebugExpressionEvaluator--GetMethodProperty.md).  
  
 [Enumerating Locals](../vs140/Enumerating-Locals.md)  
 Describes how the debug engine (DE) makes a call to enumerate local variables or arguments.  
  
 [Getting Local Properties](../vs140/Getting-Local-Properties.md)  
 Describes how the DE makes a call to get the name, type, and value of one or more locals.  
  
 [Getting Local Values](../vs140/Getting-Local-Values.md)  
 Discusses obtaining the value of the local, which requires the services of a binder object given by the evaluation context.  
  
 [Evaluating Locals](../vs140/Evaluating-Locals.md)  
 Explains how locals are evaluated.  
  
## Related Sections  
 [Evaluation Context](../vs140/Evaluation-Context.md)  
 Provides the arguments that are passed when the DE calls the expression evaluator (EE).  
  
 [MyCEE Sample](assetId:///624a018b-9179-402f-9d48-3aec87b48f4f)  
 Demonstrates one implementation approach to creating an expression evaluator for the MyC language.  
  
## See Also  
 [Displaying Locals](../vs140/Displaying-Locals.md)