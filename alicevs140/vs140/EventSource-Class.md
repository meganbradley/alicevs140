---
title: "EventSource Class"
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
ms.assetid: 91f1c072-6af4-44e6-b6d8-ac6d0c688dde
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EventSource Class
Represents an event. EventSource member functions add, remove, and invoke event handlers.  
  
## Syntax  
  
```  
template<  
   typename TDelegateInterface  
>  
class EventSource;  
```  
  
#### Parameters  
 `TDelegateInterface`  
 The interface to a delegate that represents an event handler.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[EventSource::EventSource Constructor](../vs140/EventSource--EventSource-Constructor.md)|Initializes a new instance of the EventSource class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[EventSource::Add Method](../vs140/EventSource--Add-Method.md)|Appends the event handler represented by the specified delegate interface to the set of event handlers for the current EventSource object.|  
|[EventSource::GetSize Method](../vs140/EventSource--GetSize-Method.md)|Retrieves the number of event handlers associated with the current EventSource object|  
|[EventSource::InvokeAll Method](../vs140/EventSource--InvokeAll-Method.md)|Calls each event handler associated with the current EventSource object using the specified argument types and arguments.|  
|[EventSource::Remove Method](../vs140/EventSource--Remove-Method.md)|Deletes the event handler represented by the specified event registration token from the set of event handlers associated with the current EventSource object.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[EventSource::addRemoveLock_ Data Member](../vs140/EventSource--addRemoveLock_-Data-Member.md)|Synchronizes access to the [targets_](../vs140/EventSource--targets_-Data-Member.md) array when adding, removing, or invoking event handlers.|  
|[EventSource::targets_ Data Member](../vs140/EventSource--targets_-Data-Member.md)|An array of one or more event handlers.|  
|[EventSource::targetsPointerLock_ Data Member](../vs140/EventSource--targetsPointerLock_-Data-Member.md)|Synchronizes access to internal data members even while event handlers for this EventSource are being added, removed, or invoked.|  
  
## Inheritance Hierarchy  
 `EventSource`  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WRL Namespace](../vs140/Microsoft--WRL-Namespace.md)