---
title: "An unexpected error has occurred because an operating system resource required for single instance startup cannot be acquired"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0d9f2a30-ff72-4355-8060-744f22339359
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# An unexpected error has occurred because an operating system resource required for single instance startup cannot be acquired
The application could not acquire a necessary operating system resource. Some of the possible causes for this problem are:  
  
-   The application does not have permissions to create named operating-system objects.  
  
-   The common language runtime does not have permissions to create memory-mapped files.  
  
-   The application needs to access an operating-system object, but another process is using it.  
  
### To correct this error  
  
1.  Check that the application has sufficient permissions to create named operating-system objects.  
  
2.  Check that the common language runtime has sufficient permissions to create memory-mapped files.  
  
3.  Restart the computer to clear any process that may be using the resource needed to connect to the original instance application.  
  
4.  Note the circumstances under which the error occurred, and call Microsoft Product Support Services  
  
## See Also  
 [Application Page, Project Designer (Visual Basic)](../Topic/Application%20Page,%20Project%20Designer%20\(Visual%20Basic\).md)   
 [Debugger Roadmap](../vs140/Debugger-Basics.md)   
 [Product Support and Accessibility](../vs140/Talk-to-Us.md)