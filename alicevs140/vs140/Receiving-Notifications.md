---
title: "Receiving Notifications"
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
ms.assetid: 305a1103-0c87-40c8-94bc-7fbbdd52ae32
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Receiving Notifications
OLE DB provides interfaces for receiving notifications when events occur. These are described in [OLE DB Object Notifications](https://msdn.microsoft.com/en-us/library/ms725406.aspx) in the *OLE DB Programmer's Reference*. Setup of these events uses the standard COM connection-point mechanism. For example, an ATL object that wants to retrieve events through `IRowsetNotify` implements the `IRowsetNotify` interface by adding `IRowsetNotify` to the class-derived list and exposing it through a **COM_INTERFACE_ENTRY** macro.  
  
 `IRowsetNotify` has three methods, which can be called at various times. If you want to respond to only one of these methods, you can use the [IRowsetNotifyImpl](../vs140/IRowsetNotifyImpl-Class.md) class, which returns **E_NOTIMPL** for the methods you are not interested in.  
  
 When you create the rowset, you must tell the provider that you want the returned rowset object to support **IConnectionPointContainer**, which is needed to set up the notification.  
  
 The following code shows how to open the rowset from an ATL object and use the `AtlAdvise` function to set up the notification sink. `AtlAdvise` returns a cookie that is used when you call `AtlUnadvise`.  
  
```  
CDBPropSet propset(DBPROPSET_ROWSET);  
propset.AddProperty(DBPROP_IConnectionPointContainer, true);  
  
product.Open(session, _T("Products"), &propset);  
  
AtlAdvise(product.m_spRowset, GetUnknown(), IID_IRowsetNotify, &m_dwCookie);  
```  
  
## See Also  
 [Using Accessors](../vs140/Using-Accessors.md)