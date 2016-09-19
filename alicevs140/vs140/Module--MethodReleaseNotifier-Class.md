---
title: "Module::MethodReleaseNotifier Class"
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
ms.assetid: 5c2902be-964b-488f-9f1c-adf504995cbc
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::MethodReleaseNotifier Class
Invokes an event handler when the last object in the current module is released. The event handler is specified by an object and its pointer-to-a-method member.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
class MethodReleaseNotifier : public ReleaseNotifier;  
```  
  
#### Parameters  
 `T`  
 The type of the object whose member function is the event handler.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[Module::MethodReleaseNotifier::MethodReleaseNotifier Constructor](../vs140/Module--MethodReleaseNotifier--MethodReleaseNotifier-Constructor.md)|Initializes a new instance of the Module::MethodReleaseNotifier class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Module::MethodReleaseNotifier::Invoke Method](../vs140/Module--MethodReleaseNotifier--Invoke-Method.md)|Calls the event handler associated with the current Module::MethodReleaseNotifier object.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[Module::MethodReleaseNotifier::method_ Data Member](../vs140/Module--MethodReleaseNotifier--method_-Data-Member.md)|Holds a pointer to the event handler for the current Module::MethodReleaseNotifier object.|  
|[Module::MethodReleaseNotifier::object_ Data Member](../vs140/Module--MethodReleaseNotifier--object_-Data-Member.md)|Holds a pointer to the object whose member function is the event handler for the current Module::MethodReleaseNotifier object.|  
  
## Inheritance Hierarchy  
 `ReleaseNotifier`  
  
 `MethodReleaseNotifier`  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)