---
title: "Data Sources and Sessions"
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
ms.assetid: 6ee52216-e082-4869-a1d6-ce561cfb76e5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Sources and Sessions
The following figure shows the classes that support connecting to and accessing a data source. Each class is based on a standard OLE DB component implementation.  
  
 ![Data source and session classes](../vs140/media/vcDataSourceSessionClasses.gif "vcDataSourceSessionClasses")  
Data Source and Session Classes  
  
 The classes are:  
  
-   [CDataSource](../vs140/CDataSource-Class.md) This class instantiates the data source object, which creates and manages a connection to a data source through an OLE DB provider. The data source takes information such as the data source address and authentication information in the form of a connection string.  
  
     It is also worth noting that the helper class [CEnumerator](../vs140/CEnumerator-Class.md) is often used before any connection is established to obtain a list of available providers registered on a system. This allows you to select a provider as a data source. For example, the **Data Link Properties** dialog box uses this class to populate the list of providers on the **Providers** tab. It is equivalent to the **SQLBrowseConnect** or **SQLDriverConnect** function.  
  
-   [CSession](../vs140/CSession-Class.md) This class instantiates the session object, which represents a single access session to the data source. However, you can create multiple sessions on a data source. For each session, you can create rowsets, commands, and other objects to access data from the data source. The session handles transactions.  
  
## See Also  
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)