---
title: "Differences Between Applications and DLLs"
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
ms.assetid: 8f271523-d8d0-4ad1-84d2-0c5645d7fd5b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Differences Between Applications and DLLs
Even though DLLs and applications are both executable program modules, they differ in several ways. To the end user, the most obvious difference is that DLLs are not programs that can be directly executed. From the system's point of view, there are two fundamental differences between applications and DLLs:  
  
-   An application can have multiple instances of itself running in the system simultaneously, whereas a DLL can have only one instance.  
  
-   An application can own things such as a stack, global memory, file handles, and a message queue, but a DLL cannot.  
  
## What do you want to do?  
  
-   [Export from a DLL](../vs140/Exporting-from-a-DLL.md)  
  
-   [Link an executable to a DLL](../vs140/Linking-an-Executable-to-a-DLL.md)  
  
-   [Initialize a DLL](../vs140/Initializing-a-DLL.md)  
  
## What do you want to know more about?  
  
-   [The advantages of using DLLs](../vs140/Advantages-of-Using-DLLs.md)  
  
-   [Non-MFC DLLs: Overview](../vs140/Non-MFC-DLLs--Overview.md)  
  
-   [Regular DLLs statically linked to MFC](../vs140/Regular-DLLs-Statically-Linked-to-MFC.md)  
  
-   [Regular DLLs dynamically linked to MFC](../vs140/Regular-DLLs-Dynamically-Linked-to-MFC.md)  
  
-   [Extension DLLs: Overview](../vs140/Extension-DLLs--Overview.md)  
  
## See Also  
 [DLLs in Visual C++](../vs140/DLLs-in-Visual-C--.md)