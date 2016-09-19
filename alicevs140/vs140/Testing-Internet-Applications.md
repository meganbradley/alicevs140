---
title: "Testing Internet Applications"
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
ms.assetid: ac4c74e3-d4ad-4e19-8f6c-e270de067f01
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Testing Internet Applications
There are some unique testing challenges on the Internet, especially for applications running on a Web server. Your initial testing will probably be done using a single-user client connecting to a test server. This will be useful for debugging your code.  
  
 You will also want to test under real conditions: with multiple clients connected over high-speed connections as well as low-speed serial lines, including modem connections. It can be difficult to simulate real conditions, but it is certainly worth spending time designing possible scenarios and executing them. If possible, you will also want to use tools to do capacity and stress testing. Certain classes of bugs, such as timing bugs, are difficult to find and to reproduce.  
  
 One of the challenges of Internet programming is its visibility. Many accesses to your site may slow down your server. You want your server to degrade gracefully. You want to prevent anything that could be destructive to a user's computer if your application fails (for example, corruption of data while writing to the registry or while writing cookies on the client).  
  
## See Also  
 [MFC Internet Programming Tasks](../vs140/MFC-Internet-Programming-Tasks.md)   
 [MFC Internet Programming Basics](../vs140/MFC-Internet-Programming-Basics.md)