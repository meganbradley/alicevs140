---
title: "OLE DB Resource Pooling and Services"
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
ms.assetid: 360c36e2-25ae-4caf-8ee7-d4a6b6898f68
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OLE DB Resource Pooling and Services
To work well with OLE DB pooling, or with any OLE DB service, your provider must support aggregation of all objects. This is a requirement of any OLE DB 1.5 or later provider. It is critical for leveraging services. Providers that do not support aggregation cannot be pooled and no additional services are provided.  
  
 To be pooled, providers must support the free thread model. The resource pool determines the provider's thread model according to the **DBPROP_THREADMODEL** property.  
  
 If the provider has a global connection state that might change while the data source is in an initialized state, it should support the new **DBPROP_RESETDATASOURCE** property. This property is called before a connection is reused and gives the provider the opportunity to clean up state before its next use. If the provider cannot clean up some state associated with the connection, it can return **DBPROPSTATUS_NOTSETTABLE** for the property and the connection will not be reused.  
  
 Providers that connect to a remote database and can detect whether that connection might be lost should support the **DBPROP_CONNECTIONSTATUS** property. This property gives the OLE DB services the ability to detect dead connections and make sure they are not returned to the pool.  
  
 Finally, automatic transaction enlistment generally does not work unless it is implemented at the same level that pooling occurs. Providers that support automatic transaction enlistment themselves should support disabling this enlistment by exposing the **DBPROP_INIT_OLEDBSERVICES** property and disabling enlistment if the **DBPROPVAL_OS_TXNENLISTMENT** is deselected.  
  
## See Also  
 [Advanced Provider Techniques](../vs140/Advanced-Provider-Techniques.md)