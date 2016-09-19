---
title: "Command Routing"
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
ms.assetid: 9393a956-bdd4-47c5-9013-dbd680433f93
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command Routing
Your responsibility in working with commands is limited to making message-map connections between commands and their handler functions, a task for which you use the Properties window. You must also write most command handlers.  
  
 Windows messages are usually sent to the main frame window, but command messages are then routed to other objects. The framework routes commands through a standard sequence of command-target objects, one of which is expected to have a handler for the command. Each command-target object checks its message map to see if it can handle the incoming message.  
  
 Different command-target classes check their own message maps at different times. Typically, a class routes the command to certain other objects to give them first chance at the command. If none of those objects handles the command, the original class checks its own message map. Then, if it can't supply a handler itself, it may route the command to yet more command targets. The table [Standard Command Route](#_core_standard_command_route) below shows how each of the classes structures this sequence. The general order in which a command target routes a command is:  
  
1.  To its currently active child command-target object.  
  
2.  To itself.  
  
3.  To other command targets.  
  
 How expensive is this routing mechanism? Compared to what your handler does in response to a command, the cost of the routing is low. Bear in mind that the framework generates commands only when the user interacts with a user-interface object.  
  
### Standard Command Route  
  
|When an object of this type receives a command . . .|It gives itself and other command-target objects a chance to handle the command in this order:|  
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|  
|MDI frame window  (`CMDIFrameWnd`)|1.  Active `CMDIChildWnd`<br />2.  This frame window<br />3.  Application (`CWinApp` object)|  
|Document frame window  (`CFrameWnd`, `CMDIChildWnd`)|1.  Active view<br />2.  This frame window<br />3.  Application (`CWinApp` object)|  
|View|1.  This view<br />2.  Document attached to the view|  
|Document|1.  This document<br />2.  Document template attached to the document|  
|Dialog box|1.  This dialog box<br />2.  Window that owns the dialog box<br />3.  Application (`CWinApp` object)|  
  
 Where numbered entries in the second column of the preceding table mention other objects, such as a document, see the corresponding item in the first column. For instance, when you read in the second column that the view forwards a command to its document, see the "Document" entry in the first column to follow the routing further.  
  
## See Also  
 [How the Framework Calls a Handler](../vs140/How-the-Framework-Calls-a-Handler.md)