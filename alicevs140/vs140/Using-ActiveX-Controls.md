---
title: "Using ActiveX Controls"
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
ms.assetid: 33442173-205d-492f-82c8-9a8105358ec6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using ActiveX Controls
The topics in this section present an overview of using ActiveX controls.  
  
 An ActiveX control is a COM component that supports standard interfaces relating to persistence, connection points, and hosting. These standard interfaces define a protocol by which a control can be hosted in a control container, exchange messages, and handle events.  
  
 As COM servers, ActiveX controls have the following.  
  
|Term|Description|  
|----------|-----------------|  
|Properties|Controls have member variables to represent internal state and are implemented as **Get** and `Set` accessor functions. A **Get** function is generated for each accessor method with a propget tag in the .idl file. A `Set` function is generated for each accessor method with either a propput or propputref IDL tag.<br /><br /> Use [wrapper classes](../vs140/Wrapper-Classes.md) or the [OLE/COM Object Viewer](../vs140/Using-the-OLE-COM-Object-Viewer.md) to determine how accessor functions are defined.|  
|Methods|A control's behavior is defined by its public methods. Wrapper classes give you access to a control's methods.<br /><br /> If you do not use wrapper classes (the default), you get access to a control's methods by obtaining a pointer to an interface.<br /><br /> An example of a public method is the **Refresh** method in the ADO data control, which updates the retrieved rowset.|  
|Events|A control can generate an event to notify the host that something happened. An example is the `OnClick` event for the Button control. When the button gets clicked, the button generates an `OnClick` event. If the control's host has a handler for that event, it executes.|  
|Type Library|A type library tells a control container what properties, methods, and events are supported by a control. Type libraries can exist either as separate files (with a .tlb extension) or internally within the control.<br /><br /> Type libraries also contain the control's coclass information. A coclass is a COM class that is identified with a GUID. A coclass contains one or more interfaces that are defined by the control.<br /><br /> To examine type libraries, use the [OLE/COM Object Viewer](../vs140/Using-the-OLE-COM-Object-Viewer.md).|  
  
 The following topics describe the use of an ActiveX control:  
  
-   [Inserting the Control into a Visual C++ Application](../vs140/Inserting-the-Control-into-a-Visual-C---Application.md)  
  
-   [Wrapper Classes](../vs140/Wrapper-Classes.md)  
  
-   [Creating a Database Connection](../vs140/Creating-Database-Connections.md)  
  
-   [Setting Control Properties at Design Time](../vs140/Setting-Control-Properties-at-Design-Time.md)  
  
-   [Setting Event Handlers on ActiveX Controls](../vs140/Setting-Event-Handlers-on-ActiveX-Controls.md)  
  
-   [Modifying a Control's Run-Time Behavior](../vs140/Modifying-a-Control-s-Run-Time-Behavior.md)  
  
-   [Redistributing Controls](../vs140/Redistributing-Controls.md)  
  
## See Also  
 [Data-Bound Controls (ADO and RDO)](../vs140/Data-Bound-Controls--ADO-and-RDO-.md)