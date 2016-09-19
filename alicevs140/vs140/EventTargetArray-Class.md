---
title: "EventTargetArray Class"
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
ms.assetid: e3cadb7c-2160-4cbb-a2f8-c28733d1e96d
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EventTargetArray Class
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
class EventTargetArray : public Microsoft::WRL::RuntimeClass<Microsoft::WRL::RuntimeClassFlags<ClassicCom>, IUnknown>;  
```  
  
## Remarks  
 Represents an array of event handlers.  
  
 The event handlers that are associated with an [EventSource](../vs140/EventSource-Class.md) object are stored in a protected EventTargetArray data member.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[EventTargetArray::EventTargetArray Constructor](../vs140/EventTargetArray--EventTargetArray-Constructor.md)|Initializes a new instance of the EventTargetArray class.|  
|[EventTargetArray::~EventTargetArray Destructor](../vs140/EventTargetArray--~EventTargetArray-Destructor.md)|Deinitializes the current EventTargetArray class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[EventTargetArray::AddTail Method](../vs140/EventTargetArray--AddTail-Method.md)|Appends the specified event handler to the end of the internal array of event handlers.|  
|[EventTargetArray::Begin Method](../vs140/EventTargetArray--Begin-Method.md)|Gets the address of the first element in the internal array of event handlers.|  
|[EventTargetArray::End Method](../vs140/EventTargetArray--End-Method.md)|Gets the address of the last element in the internal array of event handlers.|  
|[EventTargetArray::Length Method](../vs140/EventTargetArray--Length-Method.md)|Gets the current number of elements in the internal array of event handlers.|  
  
## Inheritance Hierarchy  
 `EventTargetArray`  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)