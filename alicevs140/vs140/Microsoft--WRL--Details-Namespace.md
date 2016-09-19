---
title: "Microsoft::WRL::Details Namespace"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: d71fe149-d804-4c6f-961d-43fe21ef8630
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft::WRL::Details Namespace
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
namespace Microsoft::WRL::Details;  
```  
  
## Members  
  
### Classes  
  
|Name|Description|  
|----------|-----------------|  
|[ComPtrRef Class](../vs140/ComPtrRef-Class.md)|Represents a reference to an object of type ComPtr<T\>.|  
|[ComPtrRefBase Class](../vs140/ComPtrRefBase-Class.md)|Represents the base class for the [ComPtrRef](../vs140/ComPtrRef-Class.md) class.|  
|[DontUseNewUseMake Class](../vs140/DontUseNewUseMake-Class.md)|Prevents using operator `new` in `RuntimeClass`. Consequently, you must use the [Make function](../vs140/Make-Function.md) instead.|  
|[EventTargetArray Class](../vs140/EventTargetArray-Class.md)|Represents an array of event handlers.|  
|[MakeAllocator Class](../vs140/MakeAllocator-Class.md)|Allocates memory for an activatable class, with or without weak reference support.|  
|[ModuleBase Class](../vs140/ModuleBase-Class.md)|Represents the base class of the [Module](../vs140/Module-Class.md) classes.|  
|[RemoveIUnknown Class](../vs140/RemoveIUnknown-Class.md)|Makes a type that is equivalent to an `IUnknown`-based type, but has non-virtual `QueryInterface`, `AddRef`, and `Release` methods.|  
|[WeakReference Class](../vs140/WeakReference-Class.md)|Represents a *weak reference* that can be used with the Windows Runtime or classic COM. A weak reference represents an object that might or might not be accessible.|  
  
### Structures  
  
|Name|Description|  
|----------|-----------------|  
|[ArgTraits Structure](../vs140/ArgTraits-Structure.md)|Declares a specified delegate interface and an anonymous member function that has a specified number of parameters.|  
|[ArgTraitsHelper Structure](../vs140/ArgTraitsHelper-Structure.md)|Helps define common characteristics of delegate arguments.|  
|[BoolStruct Structure](../vs140/BoolStruct-Structure.md)|Defines whether a ComPtr is managing the object lifetime of an interface. BoolStruct is used internally by the [BoolType()](../vs140/ComPtr--operator-Microsoft--WRL--Details--BoolType-Operator.md) operator.|  
|[CreatorMap Structure](../vs140/CreatorMap-Structure.md)|Contains information about how to initialize, register, and unregister objects.|  
|[DerefHelper Structure](../vs140/DerefHelper-Structure.md)|Represent a dereferenced pointer to the `T*` template parameter.|  
|[EnableIf Structure](../vs140/EnableIf-Structure.md)|Defines a data member of the type specified by the second template parameter if the first template parameter evaluates to `true`.|  
|[FactoryCache Structure](../vs140/FactoryCache-Structure.md)|Contains the location of a class factory and a value that identifies a registered [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] or COM class object.|  
|[ImplementsBase Structure](../vs140/ImplementsBase-Structure.md)|Used to validate template parameter types in [Implements Structure](../vs140/Implements-Structure.md).|  
|[ImplementsHelper Structure](../vs140/ImplementsHelper-Structure.md)|Helps implement the [Implements](../vs140/Implements-Structure.md) structure.|  
|[InterfaceList Structure](../vs140/InterfaceList-Structure.md)|Used to create a recursive list of interfaces.|  
|[InterfaceListHelper Structure](../vs140/InterfaceListHelper-Structure.md)|Builds an `InterfaceList` type by recursively applying the specified template parameter arguments.|  
|[InterfaceTraits Structure](../vs140/InterfaceTraits-Structure.md)|Implements common characteristics of an interface.|  
|[InvokeHelper Structure](../vs140/InvokeHelper-Structure.md)|Provides an implementation of the Invoke() method based on the specified number and type of arguments.|  
|[IsBaseOfStrict Structure](../vs140/IsBaseOfStrict-Structure.md)|Tests whether one type is the base of another.|  
|[IsSame Structure](../vs140/IsSame-Structure.md)|Tests whether one specified type is the same as another specified type.|  
|[Nil Structure](../vs140/Nil-Structure.md)|Used to indicate an unspecified, optional template parameter.|  
|[RemoveReference Structure](../vs140/RemoveReference-Structure.md)|Strips the reference or rvalue-reference trait from the specified class template parameter.|  
|[RuntimeClassBase Structure](../vs140/RuntimeClassBase-Structure.md)|Used to detect `RuntimeClass` in the [Make](../vs140/Make-Function.md) function.|  
|[RuntimeClassBaseT Structure](../vs140/RuntimeClassBaseT-Structure.md)|Provides helper methods for `QueryInterface` operations and getting interface IDs.|  
|[VerifyInheritanceHelper Structure](../vs140/VerifyInheritanceHelper-Structure.md)|Tests whether one interface is derived from another interface.|  
|[VerifyInterfaceHelper Structure](../vs140/VerifyInterfaceHelper-Structure.md)|Verifies that the interface specified by the template parameter meets certain requirements.|  
  
### Enumerations  
  
|Name|Description|  
|----------|-----------------|  
|[AsyncStatusInternal Enumeration](../vs140/AsyncStatusInternal-Enumeration.md)|Specifies a mapping between internal enumerations for the state of asynchronous operations and the **Windows::Foundation::AsyncStatus** enumeration.|  
  
### Functions  
  
|Name|Description|  
|----------|-----------------|  
|[ActivationFactoryCallback Function](../vs140/ActivationFactoryCallback-Function.md)|Gets the activation factory for the specified activation ID.|  
|[Move Function](../vs140/Move-Function.md)|Moves the specified argument from one location to another.|  
|[RaiseException Function](../vs140/RaiseException-Function.md)|Raises an exception in the calling thread.|  
|[Swap Function](../vs140/Swap-Function--Windows-Runtime-C---Template-Library-.md)|Exchanges the values of the two specified arguments.|  
|[TerminateMap Function](../vs140/TerminateMap-Function.md)|Shuts down the class factories in the specified module.|  
  
## Requirements  
 **Header:** async.h, client.h, corewrappers.h, event.h, ftm.h, implements.h, internal.h, module.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)   
 [Microsoft::WRL::Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)