---
title: "Key WRL APIs by Category"
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
ms.assetid: 7367bacf-6b7c-4ecd-a0ce-a662db46fc66
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Key WRL APIs by Category
The following tables list primary [!INCLUDE[cppwrl](../vs140/includes/cppwrl_md.md)] classes, structs, functions, and macros. Constructs in helper namespaces and classes are omitted. These lists augment the API documentation, which is arranged by namespace.  
  
### Classes  
  
|Title|Description|  
|-----------|-----------------|  
|[ActivationFactory Class](../vs140/ActivationFactory-Class.md)|Enables one or more classes to be activated by the Windows Runtime.|  
|[AsyncBase Class](../vs140/AsyncBase-Class.md)|Implements the Windows Runtime asynchronous state machine.|  
|[ClassFactory Class](../vs140/ClassFactory-Class.md)|Implements the basic functionality of the `IClassFactory` interface.|  
|[ComPtr Class](../vs140/ComPtr-Class.md)|Creates a *smart pointer* type that represents the interface specified by the template parameter. ComPtr automatically maintains a reference count for the underlying interface pointer and releases the interface when the reference count goes to zero.|  
|[Event Class](../vs140/Event-Class--Windows-Runtime-C---Template-Library-.md)|Represents an event.|  
|[EventSource Class](../vs140/EventSource-Class.md)|Represents an event. `EventSource` member functions add, remove, and invoke event handlers.|  
|[FtmBase Class](../vs140/FtmBase-Class.md)|Represents a free-threaded marshaler object.|  
|[HandleT Class](../vs140/HandleT-Class.md)|Represents a handle to an object.|  
|[HString Class](../vs140/HString-Class.md)|Provides support for manipulating HSTRING handles.|  
|[HStringReference Class](../vs140/HStringReference-Class.md)|Represents an HSTRING that is created from an existing string.|  
|[Module Class](../vs140/Module-Class.md)|Represents a collection of related objects.|  
|[Module::GenericReleaseNotifier Class](../vs140/Module--GenericReleaseNotifier-Class.md)|Invokes an event handler when the last object in the current module is released. The event handler is specified by on a lambda, functor, or pointer-to-function.|  
|[Module::MethodReleaseNotifier Class](../vs140/Module--MethodReleaseNotifier-Class.md)|Invokes an event handler when the last object in the current module is released. The event handler is specified by an object and its pointer-to-a-method member.|  
|[Module::ReleaseNotifier Class](../vs140/Module--ReleaseNotifier-Class.md)|Invokes an event handler when the last object in a module is released.|  
|[RoInitializeWrapper Class](../vs140/RoInitializeWrapper-Class.md)|Initializes the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].|  
|[RuntimeClass Class](../vs140/RuntimeClass-Class.md)|Represents an instantiated class that inherits the specified number of interfaces, and provides the specified Windows Runtime, classic COM, and weak reference support.|  
|[SimpleActivationFactory Class](../vs140/SimpleActivationFactory-Class.md)|Provides a fundamental mechanism to create a Windows Runtime or classic COM base class.|  
|[SimpleClassFactory Class](../vs140/SimpleClassFactory-Class.md)|Provides a fundamental mechanism to create a base class.|  
|[WeakRef Class](../vs140/WeakRef-Class.md)|Represents a *weak reference* that can be used by only the Windows Runtime, not classic COM. A weak reference represents an object that might or might not be accessible.|  
  
### Structures  
  
|Title|Description|  
|-----------|-----------------|  
|[ChainInterfaces Structure](../vs140/ChainInterfaces-Structure.md)|Specifies verification and initialization functions that can be applied to a set of interface IDs.|  
|[CloakedIid Structure](../vs140/CloakedIid-Structure.md)|Indicates to the `RuntimeClass`, `Implements` and `ChainInterfaces` templates that the specified interface is not accessible in the IID list.|  
|[Implements Structure](../vs140/Implements-Structure.md)|Implements `QueryInterface` and `GetIid` for the specified interfaces.|  
|[MixIn Structure](../vs140/MixIn-Structure.md)|Ensures that a runtime class derives from Windows Runtime interfaces, if any, and then classic COM interfaces.|  
  
### Functions  
  
|Title|Description|  
|-----------|-----------------|  
|[ActivateInstance Function](../vs140/ActivateInstance-Function.md)|Registers and retrieves an instance of a specified type defined in a specified class ID.|  
|[AsWeak Function](../vs140/AsWeak-Function.md)|Retrieves a weak reference to a specified instance.|  
|[Callback Function](../vs140/Callback-Function--Windows-Runtime-C---Template-Library-.md)|Creates an object whose member function is a callback method.|  
|[CreateActivationFactory Function](../vs140/CreateActivationFactory-Function.md)|Creates a factory that produces instances of the specified class that can be activated by the Windows Runtime.|  
|[CreateClassFactory Function](../vs140/CreateClassFactory-Function.md)|Creates a factory that produces instances of the specified class.|  
|[GetActivationFactory Function](../vs140/GetActivationFactory-Function.md)|Retrieves an activation factory for the type specified by the template parameter.|  
|[Make Function](../vs140/Make-Function.md)|Initializes the specified [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] class.|  
  
### Macros  
  
|Title|Description|  
|-----------|-----------------|  
|[ActivatableClass Macros](../vs140/ActivatableClass-Macros.md)|Populates an internal cache that contains a factory that can create an instance of the specified class.|  
|[InspectableClass Macro](../vs140/InspectableClass-Macro.md)|Sets the runtime class name and trust level.|  
  
## See Also  
 [Windows Runtime C++ Template Library](../vs140/Windows-Runtime-C---Template-Library--WRL-.md)