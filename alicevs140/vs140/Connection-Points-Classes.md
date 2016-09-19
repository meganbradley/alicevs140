---
title: "Connection Points Classes"
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
ms.assetid: 076365fa-299a-4dce-84c3-a5dff0e0da1f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Connection Points Classes
The following classes provide support for connection points:  
  
-   [IConnectionPointContainerImpl](../vs140/IConnectionPointContainerImpl-Class.md) Implements a connection point container.  
  
-   [IConnectionPointImpl](../vs140/IConnectionPointImpl-Class.md) Implements a connection point.  
  
-   [IPropertyNotifySinkCP](../vs140/IPropertyNotifySinkCP-Class.md) Implements a connection point representing the [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) interface.  
  
-   [CComDynamicUnkArray](../vs140/CComDynamicUnkArray-Class.md) Manages unlimited connections between a connection point and its sinks.  
  
-   [CComUnkArray](../vs140/CComUnkArray-Class.md) Manages a fixed number of connections between a connection point and its sinks.  
  
-   [CFirePropNotifyEvent](../vs140/CFirePropNotifyEvent-Class.md) Notifies a client's sink that an object's property has changed or is about to change.  
  
-   [IDispEventImpl](../vs140/IDispEventImpl-Class.md) Provides support for connection points for an ATL COM object. These connection points are mapped with an event sink map, which is provided by your COM object.  
  
-   [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md) Works in conjunction with the event sink map in your class to route events to the appropriate handler function.  
  
## Related Articles  
 [Connection Points](../vs140/ATL-Connection-Points.md)  
  
 [Event Handling and ATL](../vs140/Event-Handling-and-ATL.md)  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Connection Point Macros](../vs140/Connection-Point-Macros.md)   
 [Connection Point Global Functions](../vs140/Connection-Point-Global-Functions.md)