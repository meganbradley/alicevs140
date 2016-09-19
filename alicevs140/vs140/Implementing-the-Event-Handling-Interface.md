---
title: "Implementing the Event Handling Interface"
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
ms.assetid: eb2a5b33-88dc-4ce3-bee0-c5c38ea050d7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implementing the Event Handling Interface
ATL helps you with all three elements required for handling events: implementing the event interface, advising the event source, and unadvising the event source. The precise steps you'll need to take depend on the type of the event interface and the performance requirements of your application.  
  
 The most common ways of implementing an interface using ATL are:  
  
-   Deriving from a custom interface directly.  
  
-   Deriving from [IDispatchImpl](../vs140/IDispatchImpl-Class.md) for dual interfaces described in a type library.  
  
-   Deriving from [IDispEventImpl](../vs140/IDispEventImpl-Class.md) for dispinterfaces described in a type library.  
  
-   Deriving from [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md) for dispinterfaces not described in a type library or when you want to improve efficiency by not loading the type information at run time.  
  
 If you are implementing a custom or dual interface, you should advise the event source by calling [AtlAdvise](../vs140/AtlAdvise.md) or [CComPtrBase::Advise](../vs140/CComPtrBase--Advise.md). You will need to keep track of the cookie returned by the call yourself. Call [AtlUnadvise](../vs140/AtlUnadvise.md) to break the connection.  
  
 If you are implementing a dispinterface using `IDispEventImpl` or `IDispEventSimpleImpl`, you should advise the event source by calling [IDispEventSimpleImpl::DispEventAdvise](../vs140/IDispEventSimpleImpl--DispEventAdvise.md). Call [IDispEventSimpleImpl::DispEventUnadvise](../vs140/IDispEventSimpleImpl--DispEventUnadvise.md) to break the connection.  
  
 If you are using `IDispEventImpl` as a base class of a composite control, the event sources listed in the sink map will be advised and unadvised automatically using [CComCompositeControl::AdviseSinkMap](../vs140/CComCompositeControl--AdviseSinkMap.md).  
  
 The `IDispEventImpl` and `IDispEventSimpleImpl` classes manage the cookie for you.  
  
## See Also  
 [Event Handling](../vs140/Event-Handling-and-ATL.md)