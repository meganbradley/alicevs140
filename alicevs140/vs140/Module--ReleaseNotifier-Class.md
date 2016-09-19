---
title: "Module::ReleaseNotifier Class"
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
ms.assetid: 17249cd1-4d88-42e3-8146-da9e942d12bd
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::ReleaseNotifier Class
Invokes an event handler when the last object in a module is released.  
  
## Syntax  
  
```  
class ReleaseNotifier;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[Module::ReleaseNotifier::~ReleaseNotifier Destructor](../vs140/Module--ReleaseNotifier--~ReleaseNotifier-Destructor.md)|Deinitializes the current instance of the Module::ReleaseNotifier class.|  
|[Module::ReleaseNotifier::ReleaseNotifier Constructor](../vs140/Module--ReleaseNotifier--ReleaseNotifier-Constructor.md)|Initializes a new instance of the Module::ReleaseNotifier class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Module::ReleaseNotifier::Invoke Method](../vs140/Module--ReleaseNotifier--Invoke-Method.md)|When implemented, calls an event handler when the last object in a module is released.|  
|[Module::ReleaseNotifier::Release Method](../vs140/Module--ReleaseNotifier--Release.md)|Deletes the current Module::ReleaseNotifier object if the object was constructed with a parameter of `true`.|  
  
## Inheritance Hierarchy  
 `ReleaseNotifier`  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)