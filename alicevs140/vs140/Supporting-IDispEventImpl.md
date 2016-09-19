---
title: "Supporting IDispEventImpl"
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
ms.assetid: b957f930-6a5b-4598-8e4d-8027759957e7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Supporting IDispEventImpl
The template class [IDispEventImpl](../vs140/IDispEventImpl-Class.md) can be used to provide support for connection point sinks in your ATL class. A connection point sink allows your class to handle events fired from external COM objects. These connection point sinks are mapped with an event sink map, provided by your class.  
  
 To properly implement a connection point sink for your class, the following steps must be completed:  
  
-   Import the type libraries for each external object  
  
-   Declare the `IDispEventImpl` interfaces  
  
-   Declare an event sink map  
  
-   Advise and unadvise the connection points  
  
 The steps involved in implementing a connection point sink are all accomplished by modifying only the header file (.h) of your class.  
  
## Importing the Type Libraries  
 For each external object whose events you want to handle, you must import the type library. This step defines the events that can be handled and provides information that is used when declaring the event sink map. The [#import](../vs140/#import-Directive--C---.md) directive can be used to accomplish this. Add the necessary `#import` directive lines for each dispatch interface you will support to the header file (.h) of your class.  
  
 The following example imports the type library of an external COM server (`MSCAL.Calendar.7`):  
  
 [!CODE [NVC_ATL_Windowing#141](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#141)]  
  
> [!NOTE]
>  You must have a separate `#import` statement for each external type library you will support.  
  
## Declaring the IDispEventImpl Interfaces  
 Now that you have imported the type libraries of each dispatch interface, you need to declare separate `IDispEventImpl` interfaces for each external dispatch interface. Modify the declaration of your class by adding an `IDispEventImpl` interface declaration for each external object. For more information on the parameters, see [IDispEventImpl](../vs140/IDispEventImpl-Class.md).  
  
 The following code declares two connection point sinks, for the `DCalendarEvents` interface, for the COM object implemented by class `CMyCompositCtrl2`:  
  
 [!CODE [NVC_ATL_Windowing#142](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#142)]  
  
## Declaring an Event Sink Map  
 In order for the event notifications to be handled by the proper function, your class must route each event to its correct handler. This is achieved by declaring an event sink map.  
  
 ATL provides several macros, [BEGIN_SINK_MAP](../vs140/BEGIN_SINK_MAP.md), [END_SINK_MAP](../vs140/END_SINK_MAP.md), and [SINK_ENTRY_EX](../vs140/SINK_ENTRY.md), that make this mapping easier. The standard format is as follows:  
  
 `BEGIN_SINK_MAP(comClass)`  
  
 `SINK_ENTRY_EX(id, iid, dispid, func)`  
  
 `. . . //additional external event entries`  
  
 `END_SINK_MAP()`  
  
 The following example declares an event sink map with two event handlers:  
  
 [!CODE [NVC_ATL_Windowing#136](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#136)]  
  
 The implementation is nearly complete. The last step concerns the advising and unadvising of the external interfaces.  
  
## Advising and Unadvising the IDispEventImpl Interfaces  
 The final step is to implement a method that will advise (or unadvise) all connection points at the proper times. This advising must be done before communication between the external clients and your object can take place. Before your object becomes visible, each external dispatch interface supported by your object is queried for outgoing interfaces. A connection is established and a reference to the outgoing interface is used to handle events from the object. This procedure is referred to as "advising."  
  
 After your object is finished with the external interfaces, the outgoing interfaces should be notified that they are no longer used by your class. This process is referred to as "unadvising."  
  
 Because of the unique nature of COM objects, this procedure varies, in detail and execution, between implementations. These details are beyond the scope of this topic and are not addressed.  
  
## See Also  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)