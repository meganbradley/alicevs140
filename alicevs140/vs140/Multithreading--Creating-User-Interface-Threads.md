---
title: "Multithreading: Creating User-Interface Threads"
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
ms.assetid: 446925c1-db59-46ea-ae5b-d5ae5d5b91d8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Multithreading: Creating User-Interface Threads
A user-interface thread is commonly used to handle user input and respond to user events independently of threads executing other portions of the application. The main application thread (provided in your `CWinApp`-derived class) is already created and started for you. This topic describes the steps necessary to create additional user-interface threads.  
  
 The first thing you must do when creating a user-interface thread is derive a class from [CWinThread](../vs140/CWinThread-Class.md). You must declare and implement this class, using the [DECLARE_DYNCREATE](../vs140/DECLARE_DYNCREATE.md) and [IMPLEMENT_DYNCREATE](../vs140/IMPLEMENT_DYNCREATE.md) macros. This class must override some functions and can override others. These functions and what they should do are presented in the following table.  
  
### Functions to Override When Creating a User-Interface Thread  
  
|Function|Purpose|  
|--------------|-------------|  
|[ExitInstance](../vs140/CWinThread--ExitInstance.md)|Perform cleanup when thread terminates. Usually overridden.|  
|[InitInstance](../vs140/CWinThread--InitInstance.md)|Perform thread instance initialization. Must be overridden.|  
|[OnIdle](../vs140/CWinThread--OnIdle.md)|Perform thread-specific idle-time processing. Not usually overridden.|  
|[PreTranslateMessage](../vs140/CWinThread--PreTranslateMessage.md)|Filter messages before they are dispatched to **TranslateMessage** and **DispatchMessage**. Not usually overridden.|  
|[ProcessWndProcException](../vs140/CWinThread--ProcessWndProcException.md)|Intercept unhandled exceptions thrown by the thread's message and command handlers. Not usually overridden.|  
|[Run](../vs140/CWinThread--Run.md)|Controlling function for the thread. Contains the message pump. Rarely overridden.|  
  
 MFC provides two versions of `AfxBeginThread` through parameter overloading: one that can only create worker threads and one that can create user-interface threads or worker threads. To start your user-interface thread, call the second overload of [AfxBeginThread](../vs140/AfxBeginThread.md), providing the following information:  
  
-   The [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md) of the class you derived from `CWinThread`.  
  
-   (Optional) The desired priority level. The default is normal priority. For more information about the available priority levels, see [SetThreadPriority](http://msdn.microsoft.com/library/windows/desktop/ms686277) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)].  
  
-   (Optional) The desired stack size for the thread. The default is the same size stack as the creating thread.  
  
-   (Optional) **CREATE_SUSPENDED** if you want the thread to be created in a suspended state. The default is 0, or start the thread normally.  
  
-   (Optional) The desired security attributes. The default is the same access as the parent thread. For more information about the format of this security information, see [SECURITY_ATTRIBUTES](http://msdn.microsoft.com/library/windows/desktop/aa379560) in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)].  
  
 `AfxBeginThread` does most of the work for you. It creates a new object of your class, initializes it with the information you supply, and calls [CWinThread::CreateThread](../vs140/CWinThread--CreateThread.md) to start executing the thread. Checks are made throughout the procedure to make sure all objects are deallocated properly should any part of the creation fail.  
  
## What do you want to know more about?  
  
-   [Multithreading: Terminating Threads](../vs140/Multithreading--Terminating-Threads.md)  
  
-   [Multithreading: Creating Worker Threads](../vs140/Multithreading--Creating-Worker-Threads.md)  
  
-   [Processes and Threads](http://msdn.microsoft.com/library/windows/desktop/ms684841)  
  
## See Also  
 [Multithreading with C++ and MFC](../vs140/Multithreading-with-C---and-MFC.md)