---
title: "Servers (Visual Studio SDK)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62236d64-7956-448c-9ac3-5528f3edac1d
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Servers (Visual Studio SDK)
In terms of the debugger architecture, a **server**:  
  
-   Is a container of ports and port suppliers and is used to communicate ports and port suppliers to the session debug manager (SDM) and debug engines.  
  
-   Can identify itself by name, and enumerate its ports and port suppliers.  
  
-   Is represented by an [IDebugCoreServer2](../vs140/IDebugCoreServer2.md) interface, which is only implemented by Visual Studio (one instance of a server for each instance of Visual Studio running).  
  
## See Also  
 [Ports](../vs140/Ports.md)   
 [Port Suppliers](../vs140/Port-Suppliers.md)   
 [Debugger Concepts](../vs140/Debugger-Concepts.md)   
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)