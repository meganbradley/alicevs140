---
title: "raise"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - raise
apilocation: 
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: a3ccd3ad-f68f-4a7b-a005-c3ebfb217e8b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# raise
Sends a signal to the executing program.  
  
> [!NOTE]
>  Do not use this method to shut down a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app, except in testing or debugging scenarios. Programmatic or UI ways to close a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app are not permitted according to Section 3.6 of the [Windows 8 app certification requirements](http://go.microsoft.com/fwlink/?LinkId=262889). For more information, see [Application lifecycle (Windows Store apps)](http://go.microsoft.com/fwlink/?LinkId=262853).  
  
## Syntax  
  
```  
  
      int raise(  
int sig   
);  
```  
  
#### Parameters  
 *sig*  
 Signal to be raised.  
  
## Return Value  
 If successful, **raise** returns 0. Otherwise, it returns a nonzero value.  
  
## Remarks  
 The **raise** function sends *sig* to the executing program. If a previous call to **signal** has installed a signal-handling function for *sig*, **raise** executes that function. If no handler function has been installed, the default action associated with the signal value *sig* is taken, as follows.  
  
|Signal|Meaning|Default|  
|------------|-------------|-------------|  
|`SIGABRT`|Abnormal termination|Terminates the calling program with exit code 3|  
|`SIGFPE`|Floating-point error|Terminates the calling program|  
|`SIGILL`|Illegal instruction|Terminates the calling program|  
|`SIGINT`|CTRL+C interrupt|Terminates the calling program|  
|`SIGSEGV`|Illegal storage access|Terminates the calling program|  
|`SIGTERM`|Termination request sent to the program|Ignores the signal|  
  
 If the argument is not a valid signal as specified above, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If not handled, the function sets `errno` to `EINVAL` and returns a nonzero value.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|**raise**|<signal.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Process and Environment Control](../vs140/Process-and-Environment-Control.md)   
 [abort](../vs140/abort.md)   
 [signal](../vs140/signal.md)