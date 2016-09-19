---
title: "ATL Connection Point Classes"
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
ms.assetid: 9582ba71-7ace-4df4-9c9b-1b0636953efc
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Connection Point Classes
ATL uses the following classes to support connection points:  
  
-   [IConnectionPointImpl](../vs140/IConnectionPointImpl-Class.md) implements a connection point. The IID of the outgoing interface it represents is passed as a template parameter.  
  
-   [IConnectionPointContainerImpl](../vs140/IConnectionPointContainerImpl-Class.md) implements the connection point container and manages the list of `IConnectionPointImpl` objects.  
  
-   [IPropertyNotifySinkCP](../vs140/IPropertyNotifySinkCP-Class.md) implements a connection point representing the [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638) interface.  
  
-   [CComDynamicUnkArray](../vs140/CComDynamicUnkArray-Class.md) manages an arbitrary number of connections between the connection point and its sinks.  
  
-   [CComUnkArray](../vs140/CComUnkArray-Class.md) manages a predefined number of connections as specified by the template parameter.  
  
-   [CFirePropNotifyEvent](../vs140/CFirePropNotifyEvent-Class.md) notifies a client's sink that an object's property has changed or is about to change.  
  
-   [IDispEventImpl](../vs140/IDispEventImpl-Class.md) provides support for connection points for an ATL COM object. These connection points are mapped with an event sink map, which is provided by your COM object.  
  
-   [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md) works in conjunction with the event sink map in your class to route events to the appropriate handler function.  
  
## See Also  
 [Connection Point](../vs140/ATL-Connection-Points.md)