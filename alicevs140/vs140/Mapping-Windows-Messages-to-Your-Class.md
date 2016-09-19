---
title: "Mapping Windows Messages to Your Class"
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
ms.assetid: a4c6fd1f-1d33-47c9-baa0-001755746d6d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mapping Windows Messages to Your Class
If you need your dialog box to handle Windows messages, override the appropriate handler functions. To do so, use the Properties window to [map the messages](../vs140/Mapping-Messages-to-Functions.md) to the dialog class. This writes a message-map entry for each message and adds the message-handler member functions to the class. Use the Visual C++ source code editor to write code in the message handlers.  
  
 You can also override member functions of [CDialog](../vs140/CDialog-Class.md) and its base classes, especially [CWnd](../vs140/CWnd-Class.md).  
  
## What do you want to know more about?  
  
-   [Message handling and mapping](../vs140/Message-Handling-and-Mapping.md)  
  
-   [Commonly overridden member functions](../vs140/Commonly-Overridden-Member-Functions.md)  
  
-   [Commonly added member functions](../vs140/Commonly-Added-Member-Functions.md)  
  
## See Also  
 [Dialog Boxes](../vs140/Dialog-Boxes.md)   
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)