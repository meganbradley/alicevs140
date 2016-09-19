---
title: "OLE DB Consumers and Providers"
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
ms.assetid: 886cb39d-652b-4557-93f0-4b1b0754d8bc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OLE DB Consumers and Providers
The OLE DB architecture uses the model of consumers and providers. A consumer makes requests for data. A provider responds to these requests by placing data in a tabular format and returning it to the consumer. Any call that the consumer can make must be implemented in the provider.  
  
 Technically defined, a consumer is any system or application code (not necessarily an OLE DB component) that accesses data through OLE DB interfaces. The interfaces are implemented in a provider. Thus, a provider is any software component that implements OLE DB interfaces to encapsulate access to data and expose it to other objects (that is, consumers).  
  
 In terms of roles, a consumer calls methods on OLE DB interfaces; an OLE DB provider implements the needed OLE DB interfaces.  
  
 OLE DB avoids the terms client and server because these roles do not always make sense, especially in an n-tier situation. Because a consumer could be a component on a tier that serves another component, to call it a client component would be confusing. Also, a provider sometimes acts more like a database driver than a server.  
  
## See Also  
 [OLE DB Programming](../vs140/OLE-DB-Programming.md)   
 [OLE DB Programming Overview](../vs140/OLE-DB-Programming-Overview.md)