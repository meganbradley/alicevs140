---
title: "Advantages of Using DLLs"
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
ms.assetid: 8956c8ee-e7b3-446f-a0c6-462381747690
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Advantages of Using DLLs
Dynamic linking has the following advantages:  
  
-   Saves memory and reduces swapping. Many processes can use a single DLL simultaneously, sharing a single copy of the DLL in memory. In contrast, Windows must load a copy of the library code into memory for each application that is built with a static link library.  
  
-   Saves disk space. Many applications can share a single copy of the DLL on disk. In contrast, each application built with a static link library has the library code linked into its executable image as a separate copy.  
  
-   Upgrades to the DLL are easier. When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments and return values do not change. In contrast, statically linked object code requires that the application be relinked when the functions change.  
  
-   Provides after-market support. For example, a display driver DLL can be modified to support a display that was not available when the application was shipped.  
  
-   Supports multilanguage programs. Programs written in different programming languages can call the same DLL function as long as the programs follow the function's calling convention. The programs and the DLL function must be compatible in the following ways: the order in which the function expects its arguments to be pushed onto the stack, whether the function or the application is responsible for cleaning up the stack, and whether any arguments are passed in registers.  
  
-   Provides a mechanism to extend the MFC library classes. You can derive classes from the existing MFC classes and place them in an MFC extension DLL for use by MFC applications.  
  
-   Eases the creation of international versions. By placing resources in a DLL, it is much easier to create international versions of an application. You can place the strings for each language version of your application in a separate resource DLL and have the different language versions load the appropriate resources.  
  
 A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.  
  
## What do you want to do?  
  
-   [Export from a DLL](../vs140/Exporting-from-a-DLL.md)  
  
-   [Link an executable to a DLL](../vs140/Linking-an-Executable-to-a-DLL.md)  
  
-   [Initialize a DLL](../vs140/Initializing-a-DLL.md)  
  
## What do you want to know more about?  
  
-   [Non-MFC DLLs: Overview](../vs140/Non-MFC-DLLs--Overview.md)  
  
-   [Regular DLLs statically linked to MFC](../vs140/Regular-DLLs-Statically-Linked-to-MFC.md)  
  
-   [Regular DLLs dynamically linked to MFC](../vs140/Regular-DLLs-Dynamically-Linked-to-MFC.md)  
  
-   [Extension DLLs: Overview](../vs140/Extension-DLLs--Overview.md)  
  
## See Also  
 [DLLs in Visual C++](../vs140/DLLs-in-Visual-C--.md)