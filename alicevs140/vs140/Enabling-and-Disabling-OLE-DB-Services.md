---
title: "Enabling and Disabling OLE DB Services"
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
ms.assetid: 445f97eb-32a8-41c2-ad26-1169f78a074f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enabling and Disabling OLE DB Services
The OLE DB Service Component Manager compares the properties specified by the consumer to those supported by the provider to determine whether individual service components could be invoked to satisfy extended functionality requested by the consumer. For example, if an application requests a scrollable cursor and the provider only supports a forward-only cursor, the Service Component Manager invokes the Client Cursor Engine service component to provide scrollable functionality. If the application is relying on extended functionality supported by default on the provider's rowset, and the application does not explicitly set the properties to request that functionality, the functionality might not appear on the rowset returned by the Client Cursor Engine. To be interoperable, applications should always set properties to explicitly request extended functionality where needed.  
  
 In some cases, it might be necessary to disable individual OLE DB services to work well with existing applications that make assumptions about the characteristics of a provider. OLE DB services provide the ability to disable individual services, or all services, either on a connection-by-connection basis or for all applications using a single provider.  
  
## See Also  
 [OLE DB Resource Pooling and Services](../vs140/OLE-DB-Resource-Pooling-and-Services.md)