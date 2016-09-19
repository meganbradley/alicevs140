---
title: "IDebugManagedObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ae09d34-112c-4285-80ee-9f7f8dc414d7
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugManagedObject
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface enables the expression evaluator (EE) to call properties or methods on value class instances (for example, `System.Decimal`) and to set their value without calling [Evaluate](../vs140/IDebugFunctionObject--Evaluate.md) on the program being debugged.  
  
## Syntax  
  
```  
IDebugManagedObject : IDebugObject  
```  
  
## Notes for Implementers  
 An expression evaluator implements this interface to represent a managed code object such as a variable.  
  
## Notes for Callers  
 To obtain this interface, call [GetManagedDebugObject](../vs140/IDebugObject--GetManagedDebugObject.md) on an [IDebugObject](../vs140/IDebugObject.md) that represents an instance of a value class.  
  
## Methods in Vtable Order  
 In addition to the methods inherited from [IDebugObject](../vs140/IDebugObject.md), the `IDebugManagedObject` interface exposes the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[GetManagedObject](../vs140/IDebugManagedObject--GetManagedObject.md)|Returns an interface that represents the managed code object and from which any appropriate managed code interface can be obtained.|  
|[SetFromManagedObject](../vs140/IDebugManagedObject--SetFromManagedObject.md)|Sets the value of this object to the value of a specified managed code object.|  
  
## Remarks  
 An expression evaluator uses this interface to store a managed code object in a parse tree.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../vs140/Expression-Evaluation-Interfaces.md)   
 [Evaluate](../vs140/IDebugFunctionObject--Evaluate.md)