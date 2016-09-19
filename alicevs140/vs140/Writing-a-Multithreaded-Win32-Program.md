---
title: "Writing a Multithreaded Win32 Program"
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
ms.assetid: 1415f47d-417f-4f42-949b-946fb28aab0e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Writing a Multithreaded Win32 Program
When you write a program with multiple threads, you must coordinate their behavior and [use of the program's resources](#_core_sharing_common_resources_between_threads). You must also make sure that each thread receives [its own stack](#_core_thread_stacks).  
  
##  <a name="_core_sharing_common_resources_between_threads"></a> Sharing Common Resources Between Threads  
  
> [!NOTE]
>  For a similar discussion from the MFC point of view, see [Multithreading: Programming Tips](../vs140/Multithreading--Programming-Tips.md) and [Multithreading: When to Use the Synchronization Classes](../vs140/Multithreading--When-to-Use-the-Synchronization-Classes.md).  
  
 Each thread has its own stack and its own copy of the CPU registers. Other resources, such as files, static data, and heap memory, are shared by all threads in the process. Threads using these common resources must be synchronized. Win32 provides several ways to synchronize resources, including semaphores, critical sections, events, and mutexes.  
  
 When multiple threads are accessing static data, your program must provide for possible resource conflicts. Consider a program where one thread updates a static data structure containing *x*,*y* coordinates for items to be displayed by another thread. If the update thread alters the *x* coordinate and is preempted before it can change the *y* coordinate, the display thread might be scheduled before the *y* coordinate is updated. The item would be displayed at the wrong location. You can avoid this problem by using semaphores to control access to the structure.  
  
 A mutex (short for *mut*ual *ex*clusion) is a way of communicating among threads or processes that are executing asynchronously of one another. This communication is usually used to coordinate the activities of multiple threads or processes, typically by controlling access to a shared resource by locking and unlocking the resource. To solve this *x*,*y* coordinate update problem, the update thread sets a mutex indicating that the data structure is in use before performing the update. It would clear the mutex after both coordinates had been processed. The display thread must wait for the mutex to be clear before updating the display. This process of waiting for a mutex is often called blocking on a mutex because the process is blocked and cannot continue until the mutex clears.  
  
 The Bounce.c program shown in [Sample Multithread C Program](../vs140/Sample-Multithread-C-Program.md) uses a mutex named `ScreenMutex` to coordinate screen updates. Each time one of the display threads is ready to write to the screen, it calls **WaitForSingleObject** with the handle to `ScreenMutex` and constant **INFINITE** to indicate that the **WaitForSingleObject** call should block on the mutex and not time out. If `ScreenMutex` is clear, the wait function sets the mutex so other threads cannot interfere with the display and continues executing the thread. Otherwise, the thread blocks until the mutex clears. When the thread completes the display update, it releases the mutex by calling **ReleaseMutex**.  
  
 Screen displays and static data are only two of the resources requiring careful management. For example, your program might have multiple threads accessing the same file. Because another thread might have moved the file pointer, each thread must reset the file pointer before reading or writing. In addition, each thread must make sure that it is not preempted between the time it positions the pointer and the time it accesses the file. These threads should use a semaphore to coordinate access to the file by bracketing each file access with **WaitForSingleObject** and **ReleaseMutex** calls. The following code example illustrates this technique:  
  
```  
HANDLE    hIOMutex= CreateMutex (NULL, FALSE, NULL);  
  
WaitForSingleObject( hIOMutex, INFINITE );  
fseek( fp, desired_position, 0L );  
fwrite( data, sizeof( data ), 1, fp );  
ReleaseMutex( hIOMutex);  
```  
  
##  <a name="_core_thread_stacks"></a> Thread Stacks  
 All of an application's default stack space is allocated to the first thread of execution, which is known as thread 1. As a result, you must specify how much memory to allocate for a separate stack for each additional thread your program needs. The operating system allocates additional stack space for the thread, if necessary, but you must specify a default value.  
  
 The first argument in the `_beginthread` call is a pointer to the **BounceProc** function, which executes the threads. The second argument specifies the default stack size for the thread. The last argument is an ID number that is passed to **BounceProc**. **BounceProc** uses the ID number to seed the random number generator and to select the thread's color attribute and display character.  
  
 Threads that make calls to the C run-time library or to the Win32 API must allow sufficient stack space for the library and API functions they call. The C `printf` function requires more than 500 bytes of stack space, and you should have 2K of stack space available when calling Win32 API routines.  
  
 Because each thread has its own stack, you can avoid potential collisions over data items by using as little static data as possible. Design your program to use automatic stack variables for all data that can be private to a thread. The only global variables in the Bounce.c program are either mutexes or variables that never change after they are initialized.  
  
 Win32 also provides Thread-Local Storage (TLS) to store per-thread data. For more information, see [Thread Local Storage (TLS)](../Topic/Thread%20Local%20Storage%20\(TLS\).md).  
  
## See Also  
 [Multithreading with C and Win32](../vs140/Multithreading-with-C-and-Win32.md)