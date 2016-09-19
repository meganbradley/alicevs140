---
title: "OLE Background: Containers and Servers"
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
ms.assetid: dafbb31d-096c-4654-b774-12900d832919
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OLE Background: Containers and Servers
A container application is an application that can incorporate embedded or linked items into its own documents. The documents managed by a container application must be able to store and display OLE document components as well as the data created by the application itself. A container application must also allow users to insert new items or edit existing items by activating server applications when necessary. The user-interface requirements of a container application are listed in the article [Containers: User-Interface Issues](../vs140/Containers--User-Interface-Issues.md).  
  
 A server application or component application is an application that can create OLE document components for use by container applications. Server applications usually support drag and drop or copying their data to the Clipboard so that a container application can insert the data as an embedded or linked item. An application can be both a container and a server.  
  
 Most servers are stand-alone applications or full servers; they can either be run as stand-alone applications or can be launched by a container application. A miniserver is a special type of server application that can be launched only by a container. It cannot be run as a stand-alone application. Microsoft Draw and Microsoft Graph servers are examples of miniservers.  
  
 Containers and servers do not communicate directly. Instead, they communicate through the OLE system dynamic-link libraries (DLL). These DLLs provide functions that containers and servers call, and the containers and servers provide callback functions that the DLLs call.  
  
 Using this means of communication, a container does not need to know the implementation details of the server application. It allows a container to accept items created by any server without having to define the types of servers with which it can work. As a result, the user of a container application can take advantage of future applications and data formats. If these new applications are OLE components, then a compound document will be able to incorporate items created by those applications.  
  
## See Also  
 [OLE Background](../vs140/OLE-Background.md)   
 [OLE Background: MFC Implementation](../vs140/OLE-Background--MFC-Implementation.md)   
 [Containers](../vs140/Containers.md)   
 [Servers](../vs140/Servers.md)   
 [Containers: Client Items](../vs140/Containers--Client-Items.md)   
 [Servers: Server Items](../vs140/Servers--Server-Items.md)