---
title: "ATL Event Handling Summary"
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
ms.assetid: e8b47ef0-0bdc-47ff-9dd6-34df11dde9a2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Event Handling Summary
In general, handling COM events is a relatively simple process. There are three main steps:  
  
-   Implement the event interface on your object.  
  
-   Advise the event source that your object wants to receive events.  
  
-   Unadvise the event source when your object no longer needs to receive events.  
  
## Implementing the Interface  
 There are four main ways of implementing an interface using ATL.  
  
|Derive from|Suitable for Interface type|Requires you to implement all methods*|Requires a type library at run time|  
|-----------------|---------------------------------|---------------------------------------------|-----------------------------------------|  
|The interface|Vtable|Yes|No|  
|[IDispatchImpl](../vs140/IDispatchImpl-Class.md)|Dual|Yes|Yes|  
|[IDispEventImpl](../vs140/IDispEventImpl-Class.md)|Dispinterface|No|Yes|  
|[IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md)|Dispinterface|No|No|  
  
 \* When using ATL support classes, you are never required to implement the **IUnknown** or `IDispatch` methods manually.  
  
## Advising and Unadvising the Event Source  
 There are three main ways of advising and unadvising an event source using ATL.  
  
|Advise function|Unadvise function|Most suitable for use with|Requires you to keep track of a cookie?|Comments|  
|---------------------|-----------------------|--------------------------------|---------------------------------------------|--------------|  
|[AtlAdvise](../vs140/AtlAdvise.md), [CComPtrBase::Advise](../vs140/CComPtrBase--Advise.md)|[AtlUnadvise](../vs140/AtlUnadvise.md)|Vtable or dual interfaces|Yes|`AtlAdvise` is a global ATL function. `CComPtrBase::Advise` is used by [CComPtr](../vs140/CComPtr-Class.md) and [CComQIPtr](../vs140/CComQIPtr-Class.md).|  
|[IDispEventSimpleImpl::DispEventAdvise](../vs140/IDispEventSimpleImpl--DispEventAdvise.md)|[IDispEventSimpleImpl::DispEventUnadvise](../vs140/IDispEventSimpleImpl--DispEventUnadvise.md)|[IDispEventImpl](../vs140/IDispEventImpl-Class.md) or [IDispEventSimpleImpl](../vs140/IDispEventSimpleImpl-Class.md)|No|Fewer parameters than `AtlAdvise` since the base class does more work.|  
|[CComCompositeControl::AdviseSinkMap(TRUE)](../vs140/CComCompositeControl--AdviseSinkMap.md)|[CComCompositeControl::AdviseSinkMap(FALSE)](../vs140/CComCompositeControl--AdviseSinkMap.md)|ActiveX controls in Composite controls|No|`CComCompositeControl::AdviseSinkMap` advises all entries in the event sink map. The same function unadvises the entries. This method is called automatically by the `CComCompositeControl` class.|  
|[CAxDialogImpl::AdviseSinkMap(TRUE)](../vs140/CAxDialogImpl--AdviseSinkMap.md)|[CAxDialogImpl::AdviseSinkMap(FALSE)](../vs140/CAxDialogImpl--AdviseSinkMap.md)|ActiveX controls in a dialog box|No|`CAxDialogImpl::AdviseSinkMap` advises and unadvises all ActiveX controls in the dialog resource. This is done automatically for you.|  
  
## See Also  
 [Event Handling](../vs140/Event-Handling-and-ATL.md)   
 [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md)