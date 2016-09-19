---
title: "Exceptions: Freeing Objects in Exceptions"
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
ms.assetid: 3b14b4ee-e789-4ed2-b8e3-984950441d97
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exceptions: Freeing Objects in Exceptions
This article explains the need and the method of freeing objects when an exception occurs. Topics include:  
  
-   [Handling the exception locally](#_core_handling_the_exception_locally)  
  
-   [Throwing exceptions after destroying objects](#_core_throwing_exceptions_after_destroying_objects)  
  
 Exceptions thrown by the framework or by your application interrupt normal program flow. Thus, it is very important to keep close track of objects so that you can properly dispose of them in case an exception is thrown.  
  
 There are two primary methods to do this.  
  
-   Handle exceptions locally using the **try** and **catch** keywords, then destroy all objects with one statement.  
  
-   Destroy any object in the **catch** block before throwing the exception outside the block for further handling.  
  
 These two approaches are illustrated below as solutions to the following problematic example:  
  
 [!CODE [NVC_MFCExceptions#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#14)]  
  
 As written above, `myPerson` will not be deleted if an exception is thrown by `SomeFunc`. Execution jumps directly to the next outer exception handler, bypassing the normal function exit and the code that deletes the object. The pointer to the object goes out of scope when the exception leaves the function, and the memory occupied by the object will never be recovered as long as the program is running. This is a memory leak; it would be detected by using the memory diagnostics.  
  
##  <a name="_core_handling_the_exception_locally"></a> Handling the Exception Locally  
 The **try/catch** paradigm provides a defensive programming method for avoiding memory leaks and ensuring that your objects are destroyed when exceptions occur. For instance, the example shown earlier in this article could be rewritten as follows:  
  
 [!CODE [NVC_MFCExceptions#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#15)]  
  
 This new example sets up an exception handler to catch the exception and handle it locally. It then exits the function normally and destroys the object. The important aspect of this example is that a context to catch the exception is established with the **try/catch** blocks. Without a local exception frame, the function would never know that an exception had been thrown and would not have the chance to exit normally and destroy the object.  
  
##  <a name="_core_throwing_exceptions_after_destroying_objects"></a> Throwing Exceptions After Destroying Objects  
 Another way to handle exceptions is to pass them on to the next outer exception-handling context. In your **catch** block, you can do some cleanup of your locally allocated objects and then throw the exception on for further processing.  
  
 The throwing function may or may not need to deallocate heap objects. If the function always deallocates the heap object before returning in the normal case, then the function should also deallocate the heap object before throwing the exception. On the other hand, if the function does not normally deallocate the object before returning in the normal case, then you must decide on a case-by-case basis whether the heap object should be deallocated.  
  
 The following example shows how locally allocated objects can be cleaned up:  
  
 [!CODE [NVC_MFCExceptions#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#16)]  
  
 The exception mechanism automatically deallocates frame objects; the destructor of the frame object is also called.  
  
 If you call functions that can throw exceptions, you can use **try/catch** blocks to make sure that you catch the exceptions and have a chance to destroy any objects you have created. In particular, be aware that many MFC functions can throw exceptions.  
  
 For more information, see [Exceptions: Catching and Deleting Exceptions](../vs140/Exceptions--Catching-and-Deleting-Exceptions.md).  
  
## See Also  
 [Exception Handling](../vs140/Exception-Handling-in-MFC.md)