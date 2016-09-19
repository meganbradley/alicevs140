---
title: "Microsoft Visual Studio Debugger (Exception Thrown) Dialog Box"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fe98d10-c8f9-4b39-a920-99169bfd542e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Microsoft Visual Studio Debugger (Exception Thrown) Dialog Box
An exception has occurred in your program. This dialog box reports the kind of exception thrown. Your code needs to handle this exception. You can choose between the following options for handling the exception:  
  
 **Break**  
 Allows execution to break into the debugger. The exception handler is not invoked prior to the break. If you continue from the break, the exception handler will be invoked.  
  
 **Continue**  
 Allows execution to continue, giving the exception handler a chance to handle the exception. This option is not available for certain types of exceptions. **Continue** will allow the application to continue. In a native application, it will cause the exception to be rethrown. In a managed application, it will either cause the program to terminate or the exception to be handled by a hosting application.  
  
> [!NOTE]
>  You cannot continue after an unhandled exception in managed code. Choosing **Continue** after an unhandled exception in managed code causes debugging to stop.  
  
 **Ignore**  
 Allows execution to continue without invoking the exception handler. Because the exception handler is not invoked, this can lead to further consequences, including additional exceptions and errors. This option is not available for certain types of exceptions.  
  
## See Also  
 [Managing Exceptions with the Debugger](../Topic/Managing%20Exceptions%20with%20the%20Debugger.md)   
 [Best Practices for Handling Exceptions](assetId:///f06da765-235b-427a-bfb6-47cd219af539)   
 [Exception Handling](../vs140/Exception-Handling---C---Component-Extensions-.md)