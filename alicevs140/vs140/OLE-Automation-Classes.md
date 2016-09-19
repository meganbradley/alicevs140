---
title: "OLE Automation Classes"
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
ms.assetid: 96e5372b-ff8a-4da1-933b-4d9bbf4dceb3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OLE Automation Classes
These classes support automation clients (applications that control other applications). Automation servers (applications that can be controlled by other applications) are supported through [dispatch maps](../vs140/Dispatch-Maps.md).  
  
 [COleDispatchDriver](../vs140/COleDispatchDriver-Class.md)  
 Used to call automation servers from your automation client. When adding a class, this class is used to create type-safe classes for automation servers that provide a type library.  
  
 [COleDispatchException](../vs140/COleDispatchException-Class.md)  
 An exception resulting from an error during OLE automation. Automation exceptions are thrown by automation servers and caught by automation clients.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)