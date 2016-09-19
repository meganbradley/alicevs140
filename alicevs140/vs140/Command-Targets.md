---
title: "Command Targets"
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
ms.assetid: b0f784e5-c6dc-4391-9e71-aa7b7dcbe9f0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command Targets
The figure [Commands in the Framework](../vs140/User-Interface-Objects-and-Command-IDs.md) shows the connection between a user-interface object, such as a menu item, and the handler function that the framework calls to carry out the resulting command when the object is clicked.  
  
 Windows sends messages that are not command messages directly to a window whose handler for the message is then called. However, the framework routes commands to a number of candidate objects — called "command targets" — one of which normally invokes a handler for the command. The handler functions work the same way for both commands and standard Windows messages, but the mechanisms by which they are called are different, as explained in [How the Framework Calls a Handler](../vs140/How-the-Framework-Calls-a-Handler.md).  
  
## See Also  
 [Messages and Commands in the Framework](../vs140/Messages-and-Commands-in-the-Framework.md)