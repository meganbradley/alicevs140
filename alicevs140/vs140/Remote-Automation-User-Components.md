---
title: "Remote Automation User Components"
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
ms.assetid: 601591cc-a442-440a-988e-baf3284b0d46
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Remote Automation User Components
You will need to ensure that each client machine contains your client program and any support DLLs it requires. You will also need to ensure that the server application and any support DLLs it requires are present on the server machine. Finally, you will need to ensure that your server program is registered on each client machine before RAC Manager can be run to configure the connection. If the program is self-registering (as most will be), you need only execute the server program on the client machine to register it. Failing that, you may have to execute a registration file that you provide, or manually edit the registry.  
  
## See Also  
 [Automation Manager (MFC)](../vs140/Automation-Manager--MFC-.md)   
 [Remote Automation Connection Manager](../vs140/Remote-Automation-Connection-Manager.md)   
 [Remote Automation Installation](../vs140/Remote-Automation-Installation.md)