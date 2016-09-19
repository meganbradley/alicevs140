---
title: "Error Handling and Notification"
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
ms.assetid: b621cf60-d869-451a-b05e-dc86d78addaa
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error Handling and Notification
For more information on error handling and notification, see [Understanding the Helper Function](../vs140/Understanding-the-Helper-Function.md).  
  
 For more information on hook functions, see [Structure and Constant Definitions](../vs140/Structure-and-Constant-Definitions.md).  
  
 If your program uses delay-loaded DLLs, it must handle errors robustly since failures that occur while the program is running will result in unhandled exceptions. Failure handling is comprised of two portions:  
  
 Recovery through a hook.  
 If your code needs to recover or provide an alternate library and/or routine on failure, a hook can be provided to the helper function that can supply or remedy the situation. The hook routine needs to return a suitable value, so that processing can continue (an HINSTANCE or FARPROC) or 0 to indicate that an exception should be thrown. It could also throw its own exception or **longjmp** out of the hook. There are notification hooks and failure hooks.  
  
 Reporting via an exception.  
 If all that is necessary for handling the error is to abort the procedure, no hook is necessary as long as the user code can handle the exception.  
  
 The following topics discuss error handling and notification:  
  
-   [Notification Hooks](../vs140/Notification-Hooks.md)  
  
-   [Failure Hooks](../vs140/Failure-Hooks.md)  
  
-   [Exceptions](../vs140/Exceptions--C-C---.md)  
  
## See Also  
 [Linker Support for Delay-Loaded DLLs](../vs140/Linker-Support-for-Delay-Loaded-DLLs.md)