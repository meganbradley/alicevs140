---
title: "Module::GenericReleaseNotifier Class"
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
ms.assetid: 244a8fbe-f89b-409b-aa65-db3e37f9b125
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::GenericReleaseNotifier Class
Invokes an event handler when the last object in the current module is released. The event handler is specified by on a lambda, functor, or pointer-to-function.  
  
## Syntax  
  
```  
template<  
   typename T  
>  
class GenericReleaseNotifier : public ReleaseNotifier;  
```  
  
#### Parameters  
 `T`  
 The type of the data member that contains the location of the event handler.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[Module::GenericReleaseNotifier::GenericReleaseNotifier Constructor](../vs140/Module--GenericReleaseNotifier--GenericReleaseNotifier-Constructor.md)|Initializes a new instance of the Module::GenericReleaseNotifier class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Module::GenericReleaseNotifier::Invoke Method](../vs140/Module--GenericReleaseNotifier--Invoke-Method.md)|Calls the event handler associated with the current Module::GenericReleaseNotifier object.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[Module::GenericReleaseNotifier::callback_ Data Member](../vs140/Module--GenericReleaseNotifier--callback_-Data-Member.md)|Holds the lambda, functor, or pointer-to-function event handler associated with the current Module::GenericReleaseNotifier object.|  
  
## Inheritance Hierarchy  
 `ReleaseNotifier`  
  
 `GenericReleaseNotifier`  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)