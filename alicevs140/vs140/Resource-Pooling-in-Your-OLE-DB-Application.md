---
title: "Resource Pooling in Your OLE DB Application"
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
ms.assetid: 2ead1bcf-bbd4-43ea-a307-bb694b992fc1
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resource Pooling in Your OLE DB Application
To leverage pooling in your application, you must make sure OLE DB services are invoked by obtaining your data source through **IDataInitialize** or **IDBPromptInitialize**. If you directly use `CoCreateInstance` to invoke the provider based on the provider's CLSID, no OLE DB services are invoked.  
  
 The OLE DB services maintain pools of connected data sources as long as a reference to **IDataInitialize** or **IDBPromptInitialize** is held or as long as there is a connection in use. Pools are also maintained automatically within a COM+ 1.0 Services or Internet Information Services (IIS) environment. If your application takes advantage of pooling outside of a COM+ 1.0 Services or IIS environment, you should keep a reference to **IDataInitialize** or **IDBPromptInitialize** or hold onto at least one connection. To make sure that the pool does not get destroyed when the last connection is released by the application, keep the reference or hold on to the connection for the lifetime of your application.  
  
 OLE DB services identify the pool from which the connection is drawn at the time that `Initialize` is called. After the connection is drawn from a pool, it cannot be moved to a different pool. Therefore, avoid doing things in your application that change initialization information, such as calling `UnInitialize` or calling `QueryInterface` for a provider-specific interface before calling `Initialize`. Also, connections established with a prompt value other than **DBPROMPT_NOPROMPT** are not pooled. However, the initialization string retrieved from a connection established through prompting can be used to establish additional pooled connections to the same data source.  
  
 Some providers must make a separate connection for each session. These additional connections must be separately enlisted in the distributed transaction, if one exists. OLE DB services caches and reuses a single session per data source, but if the application requests more than one session at a time from a single data source, the provider might end up making additional connections and doing additional transaction enlistments that are not pooled. It is actually more efficient to create a separate data source for each session in a pooled environment than to create multiple sessions from a single data source.  
  
 Finally, because ADO automatically makes use of OLE DB services, you can use ADO to establish connections and the pooling and enlistment happen automatically.  
  
## See Also  
 [OLE DB Resource Pooling and Services](../vs140/OLE-DB-Resource-Pooling-and-Services.md)