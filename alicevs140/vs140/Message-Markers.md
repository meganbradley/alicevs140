---
title: "Message Markers"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 721f40ca-5af2-4a01-b8b6-2b90f6cb7f89
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Message Markers
A message marker represents log output. A message is a string that's issued by a specific thread at a specific time. You can export messages to a text file for use with other tools. You can rest the pointer on a message in the Concurrency Visualizer to view the message string. And you can view all the message markers in the [Markers Report](../vs140/Markers-Report.md).  The following illustration shows a message marker.  
  
## Message Aggregation Markers  
 Sometimes multiple messages occur so close to one another in the Concurrency Visualizer that they can’t be drawn individually. When this occurs, a *message aggregation marker* that represents the underlying messages is shown. When you rest the pointer on one of these icons, a tooltip displays the number of underlying messages that are represented. To view the messages, zoom in.  If you zoom in all the way and still get an aggregation marker, you can view the underlying messages in the [Markers Report](../vs140/Markers-Report.md).  
  
## See Also  
 [Concurrency Visualizer Markers](../vs140/Concurrency-Visualizer-Markers.md)   
 [Concurrency Visualizer SDK](../Topic/Concurrency%20Visualizer%20SDK.md)