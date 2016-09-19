---
title: "Event Maps"
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
ms.assetid: 1ed53aee-bc53-43cd-834a-6fb935c0d29b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Event Maps
Whenever a control wishes to notify its container that some action (determined by the control developer) has happened (such as a keystroke, mouse click, or a change to the control's state) it calls an event-firing function. This function notifies the control container that some important action has occurred by firing the related event.  
  
 The Microsoft Foundation Class Library offers a programming model optimized for firing events. In this model, "event maps" are used to designate which functions fire which events for a particular control. Event maps contain one macro for each event. For example, an event map that fires a stock Click event might look like this:  
  
 [!CODE [NVC_MFCAxCtl#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#16)]  
  
 The **EVENT_STOCK_CLICK** macro indicates that the control will fire a stock Click event every time it detects a mouse click. For a more detailed listing of other stock events, see the article [ActiveX Controls: Events](../vs140/MFC-ActiveX-Controls--Events.md). Macros are also available to indicate custom events.  
  
 Although event-map macros are important, you generally do not insert them directly. This is because the Properties window automatically creates event-map entries in your source files when you use it to associate event-firing functions with events. Any time you want to edit or add an event-map entry, you can use the Properties window.  
  
 To support event maps, MFC provides the following macros:  
  
### Event Map Declaration and Demarcation  
  
|||  
|-|-|  
|[DECLARE_EVENT_MAP](../vs140/DECLARE_EVENT_MAP.md)|Declares that an event map will be used in a class to map events to event-firing functions (must be used in the class declaration).|  
|[BEGIN_EVENT_MAP](../vs140/BEGIN_EVENT_MAP.md)|Begins the definition of an event map (must be used in the class implementation).|  
|[END_EVENT_MAP](../vs140/END_EVENT_MAP.md)|Ends the definition of an event map (must be used in the class implementation).|  
  
### Event Mapping Macros  
  
|||  
|-|-|  
|[EVENT_CUSTOM](../vs140/EVENT_CUSTOM.md)|Indicates which event-firing function will fire the specified event.|  
|[EVENT_CUSTOM_ID](../vs140/EVENT_CUSTOM_ID.md)|Indicates which event-firing function will fire the specified event, with a designated dispatch ID.|  
  
### Message Mapping Macros  
  
|||  
|-|-|  
|[ON_OLEVERB](../vs140/ON_OLEVERB.md)|Indicates a custom verb handled by the OLE control.|  
|[ON_STDOLEVERB](../vs140/ON_STDOLEVERB.md)|Overrides a standard verb mapping of the OLE control.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)