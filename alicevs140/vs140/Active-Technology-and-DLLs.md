---
title: "Active Technology and DLLs"
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
ms.assetid: 3ed27f8d-164a-4562-ad61-9f2333404cc7
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Active Technology and DLLs
Active technology allows object servers to be completely implemented inside a DLL. This type of server is called an in-process server. MFC does not completely support in-process servers for all the features of visual editing, mainly because Active technology does not provide a way for a server to hook into the container's main message loop. MFC requires access to the container application's message loop to handle accelerator keys and idle-time processing.  
  
 If you are writing an Automation server and your server has no user interface, you can make your server an in-process server and put it completely into a DLL.  
  
## What do you want to know more about?  
  
-   [Automation Servers](../vs140/Automation-Servers.md)  
  
## See Also  
 [DLLs in Visual C++](../vs140/DLLs-in-Visual-C--.md)