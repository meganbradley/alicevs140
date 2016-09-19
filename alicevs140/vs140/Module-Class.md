---
title: "Module Class"
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
ms.assetid: dd67e3b8-c2e1-4f53-8c0f-565a140ba649
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module Class
Represents a collection of related objects.  
  
## Syntax  
  
```  
  
template<  
   ModuleType moduleType  
>  
class Module;  
  
template<>  
class Module<InProc> : public Details::ModuleBase;  
  
template<>  
class Module<OutOfProc> : public Module<InProc>;  
```  
  
#### Parameters  
 `moduleType`  
 A combination of one or more [ModuleType](../vs140/ModuleType-Enumeration.md) enumeration values.  
  
## Members  
  
### Protected Classes  
  
|Name|Description|  
|----------|-----------------|  
|[Module::GenericReleaseNotifier Class](../vs140/Module--GenericReleaseNotifier-Class.md)|Invokes an event handler when the last object in the current module is released. The event handler is specified by on a lambda, functor, or pointer-to-function.|  
|[Module::MethodReleaseNotifier Class](../vs140/Module--MethodReleaseNotifier-Class.md)|Invokes an event handler when the last object in the current module is released. The event handler is specified by an object and its pointer-to-a-method member.|  
|[Module::ReleaseNotifier Class](../vs140/Module--ReleaseNotifier-Class.md)|Invokes an event handler when the last object in a module is released.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[Module::~Module Destructor](../vs140/Module--~Module-Destructor.md)|Deinitializes the current instance of the Module class.|  
  
### Protected Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[Module::Module Constructor](../vs140/Module--Module-Constructor.md)|Initializes a new instance of the Module class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Module::Create Method](../vs140/Module--Create-Method.md)|Creates an instance of a module.|  
|[Module::DecrementObjectCount Method](../vs140/Module--DecrementObjectCount-Method.md)|Decrements the number of objects tracked by the module.|  
|[Module::GetActivationFactory Method](../vs140/Module--GetActivationFactory-Method.md)|Gets an activation factory for the module.|  
|[Module::GetClassObject Method](../vs140/Module--GetClassObject-Method.md)|Retreives a cache of class factories.|  
|[Module::GetModule Method](../vs140/Module--GetModule-Method.md)|Creates an instance of a module.|  
|[Module::GetObjectCount Method](../vs140/Module--GetObjectCount-Method.md)|Retrieves the number of objects managed by this module.|  
|[Module::IncrementObjectCount Method](../vs140/Module--IncrementObjectCount-Method.md)|Increments the number of objects tracked by the module.|  
|[Module::RegisterCOMObject Method](../vs140/Module--RegisterCOMObject-Method.md)|Registers one or more COM objects so other applications can connect to them.|  
|[Module::RegisterObjects Method](../vs140/Module--RegisterObjects-Method.md)|Registers COM or [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] objects so other applications can connect to them.|  
|[Module::RegisterWinRTObject Method](../vs140/Module--RegisterWinRTObject-Method.md)|Registers one or more [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] objects so other applications can connect to them.|  
|[Module::Terminate Method](../vs140/Module--Terminate-Method.md)|Causes all factories instantiated by the module to shut down.|  
|[Module::UnregisterCOMObject Method](../vs140/Module--UnregisterCOMObject-Method.md)|Unregisters one or more COM objects, which prevents other applications from connecting to them.|  
|[Module::UnregisterObjects Method](../vs140/Module--UnregisterObjects-Method.md)|Unregisters the objects in the specified module so that other applications cannot connect to them.|  
|[Module::UnregisterWinRTObject Method](../vs140/Module--UnregisterWinRTObject-Method.md)|Unregisters one or more [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] objects so that other applications cannot connect to them.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Module::Create Method](../vs140/Module--Create-Method.md)|Creates an instance of a module.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[Module::objectCount_ Data Member](../vs140/Module--objectCount_-Data-Member.md)|Keeps track of how many classes have been created with the [Make](../vs140/Make-Function.md) function.|  
|[Module::releaseNotifier_ Data Member](../vs140/Module--releaseNotifier_-Data-Member.md)|Holds a pointer to a ReleaseNotifier object.|  
  
### Macros  
  
|||  
|-|-|  
|[ActivatableClass](../vs140/ActivatableClass-Macros.md)|Populates an internal cache that contains a factory that can create an instance of the specified class. This macro specifies default factory and group ID parameters.|  
|[ActivatableClassWithFactory](../vs140/ActivatableClass-Macros.md)|Populates an internal cache that contains a factory that can create an instance of the specified class. This macro enables you to specify a particular factory parameter.|  
|[ActivatableClassWithFactoryEx](../vs140/ActivatableClass-Macros.md)|Populates an internal cache that contains a factory that can create an instance of the specified class. This macro enables you to specify particular factory and group ID parameters.|  
  
## Inheritance Hierarchy  
 `ModuleBase`  
  
 `Module`  
  
 `Module`  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)