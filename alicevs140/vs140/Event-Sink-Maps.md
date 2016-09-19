---
title: "Event Sink Maps"
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
ms.topic: article
ms.assetid: a9757eb2-5f4a-45ec-a2cd-ce5eec85b16f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event Sink Maps
When an embedded OLE control fires an event, the control's container receives the event using a mechanism, called an "event sink map," supplied by MFC. This event sink map designates handler functions for each specific event, as well as parameters of those events. For more information on event sink maps, see the article [ActiveX Control Containers](../vs140/ActiveX-Control-Containers.md).  
  
### Event Sink Maps  
  
|||  
|-|-|  
|[BEGIN_EVENTSINK_MAP](../vs140/BEGIN_EVENTSINK_MAP.md)|Starts the definition of an event sink map.|  
|[DECLARE_EVENTSINK_MAP](../vs140/DECLARE_EVENTSINK_MAP.md)|Declares an event sink map.|  
|[END_EVENTSINK_MAP](../vs140/END_EVENTSINK_MAP.md)|Ends the definition of an event sink map.|  
|[ON_EVENT](../vs140/ON_EVENT.md)|Defines an event handler for a specific event.|  
|[ON_EVENT_RANGE](../vs140/ON_EVENT_RANGE.md)|Defines an event handler for a specific event fired from a set of OLE controls.|  
|[ON_EVENT_REFLECT](../vs140/ON_EVENT_REFLECT.md)|Receives events fired by the control before they are handled by the control's container.|  
|[ON_PROPNOTIFY](../vs140/ON_PROPNOTIFY.md)|Defines a handler for handling property notifications from an OLE control.|  
|[ON_PROPNOTIFY_RANGE](../vs140/ON_PROPNOTIFY_RANGE.md)|Defines a handler for handling property notifications from a set of OLE controls.|  
|[ON_PROPNOTIFY_REFLECT](../vs140/ON_PROPNOTIFY_REFLECT.md)|Receives property notifications sent by the control before they are handled by the control's container.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)