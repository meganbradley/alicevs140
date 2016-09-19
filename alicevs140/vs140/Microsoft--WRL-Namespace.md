---
title: "Microsoft::WRL Namespace"
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
ms.assetid: 01118a8f-f564-4859-b87e-9444848585a1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft::WRL Namespace
Defines the fundamental types that make up the [!INCLUDE[cppwrl_short](../vs140/includes/cppwrl_short_md.md)].  
  
## Syntax  
  
```  
namespace Microsoft::WRL;  
```  
  
## Members  
  
### Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`InhibitWeakReferencePolicy`|`RuntimeClassFlags<WinRt &#124; InhibitWeakReference>`|  
  
### Classes  
  
|Name|Description|  
|----------|-----------------|  
|[ActivationFactory Class](../vs140/ActivationFactory-Class.md)|Enables one or more classes to be activated by the Windows Runtime.|  
|[AsyncBase Class](../vs140/AsyncBase-Class.md)|Implements the Windows Runtime asynchronous state machine.|  
|[ClassFactory Class](../vs140/ClassFactory-Class.md)|Implements the basic functionality of the `IClassFactory` interface.|  
|[ComPtr Class](../vs140/ComPtr-Class.md)|Creates a *smart pointer* type that represents the interface specified by the template parameter. ComPtr automatically maintains a reference count for the underlying interface pointer and releases the interface when the reference count goes to zero.|  
|[DeferrableEventArgs Class](../vs140/DeferrableEventArgs-Class.md)|A template class used for the event argument types for deferrals.|  
|[EventSource Class](../vs140/EventSource-Class.md)|Represents an event. `EventSource` member functions add, remove, and invoke event handlers.|  
|[FtmBase Class](../vs140/FtmBase-Class.md)|Represents a free-threaded marshaler object.|  
|[Module Class](../vs140/Module-Class.md)|Represents a collection of related objects.|  
|[RuntimeClass Class](../vs140/RuntimeClass-Class.md)|Represents an instantiated class that inherits the specified number of interfaces, and provides the specified Windows Runtime, classic COM, and weak reference support.|  
|[SimpleActivationFactory Class](../vs140/SimpleActivationFactory-Class.md)|Provides a fundamental mechanism to create a Windows Runtime or classic COM base class.|  
|[SimpleClassFactory Class](../vs140/SimpleClassFactory-Class.md)|Provides a fundamental mechanism to create a base class.|  
|[WeakRef Class](../vs140/WeakRef-Class.md)|Represents a *weak reference* that can be used by only the Windows Runtime, not classic COM. A weak reference represents an object that might or might not be accessible.|  
  
### Structures  
  
|Name|Description|  
|----------|-----------------|  
|[ChainInterfaces Structure](../vs140/ChainInterfaces-Structure.md)|Specifies verification and initialization functions that can be applied to a set of interface IDs.|  
|[CloakedIid Structure](../vs140/CloakedIid-Structure.md)|Indicates to the RuntimeClass, Implements and ChainInterfaces templates that the specified interface is not accessible in the IID list.|  
|[Implements Structure](../vs140/Implements-Structure.md)|Implements QueryInterface and GetIid for the specified interfaces.|  
|[MixIn Structure](../vs140/MixIn-Structure.md)|Ensures that a runtime class derives from Windows Runtime interfaces, if any, and then classic COM interfaces.|  
|[RuntimeClassFlags Structure](../vs140/RuntimeClassFlags-Structure.md)|Contains the type for an instance of a [RuntimeClass](../vs140/RuntimeClass-Class.md).|  
  
### Enumerations  
  
|Name|Description|  
|----------|-----------------|  
|[AsyncResultType Enumeration](../vs140/AsyncResultType-Enumeration.md)|Specifies the type of result returned by the GetResults() method.|  
|[ModuleType Enumeration](../vs140/ModuleType-Enumeration.md)|Specifies whether a module should support an in-process server or an out-of-process server.|  
|[RuntimeClassType Enumeration](../vs140/RuntimeClassType-Enumeration.md)|Specifies the type of [RuntimeClass](../vs140/RuntimeClass-Class.md) instance that is supported.|  
  
### Functions  
  
|Name|Description|  
|----------|-----------------|  
|[AsWeak Function](../vs140/AsWeak-Function.md)|Retrieves a weak reference to a specified instance.|  
|[Callback Function](../vs140/Callback-Function--Windows-Runtime-C---Template-Library-.md)|Creates an object whose member function is a callback method.|  
|[CreateActivationFactory Function](../vs140/CreateActivationFactory-Function.md)|Creates a factory that produces instances of the specified class that can be activated by the Windows Runtime.|  
|[CreateClassFactory Function](../vs140/CreateClassFactory-Function.md)|Creates a factory that produces instances of the specified class.|  
|[Make Function](../vs140/Make-Function.md)|Initializes the specified [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] class.|  
  
## Requirements  
 **Header:** async.h, client.h, corewrappers.h, event.h, ftm.h, implements.h, internal.h, module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Microsoft::WRL::Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)