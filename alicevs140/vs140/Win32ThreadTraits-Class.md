---
title: "Win32ThreadTraits Class"
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
ms.topic: reference
ms.assetid: 50279c38-eae1-4301-9ea6-97ccea580f3e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Win32ThreadTraits Class
This class provides the creation function for a Windows thread. Use this class if the thread will not use CRT functions.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class Win32ThreadTraits  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Win32ThreadTraits::CreateThread](../vs140/Win32ThreadTraits--CreateThread.md)|(Static) Call this function to create a thread that should not use CRT functions.|  
  
## Remarks  
 Thread traits are classes that provide a creation function for a particular type of thread. The creation function has the same signature and semantics as the Windows [CreateThread](http://msdn.microsoft.com/library/windows/desktop/ms682453) function.  
  
 Thread traits are used by the following classes:  
  
-   [CThreadPool](../vs140/CThreadPool-Class.md)  
  
-   [CWorkerThread](../vs140/CWorkerThread-Class.md)  
  
 If the thread will be using CRT functions, use [CRTThreadTraits](../vs140/CRTThreadTraits-Class.md) instead.  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="win32threadtraits__createthread"></a>  Win32ThreadTraits::CreateThread  
 Call this function to create a thread that should not use CRT functions.  
  
```  
  
static HANDLE CreateThread(  
      LPSECURITY_ATTRIBUTES  lpsa,  
      DWORD  dwStackSize,  
      LPTHREAD_START_ROUTINE  pfnThreadProc,  
      void*  pvParam,  
      DWORD  dwCreationFlags,  
      DWORD*  pdwThreadId  
   ) throw( );  
  
```  
  
### Parameters  
 `lpsa`  
 The security attributes for the new thread.  
  
 `dwStackSize`  
 The stack size for the new thread.  
  
 `pfnThreadProc`  
 The thread procedure of the new thread.  
  
 `pvParam`  
 The parameter to be passed to the thread procedure.  
  
 `dwCreationFlags`  
 The creation flags (0 or CREATE_SUSPENDED).  
  
 `pdwThreadId`  
 [out] Address of the DWORD variable that, on success, receives the thread ID of the newly created thread.  
  
### Return Value  
 Returns the handle to the newly created thread or NULL on failure. Call [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) to get extended error information.  
  
### Remarks  
 See [CreateThread](http://msdn.microsoft.com/library/windows/desktop/ms682453) for further information on the parameters to this function.  
  
 This function calls `CreateThread` to create the thread.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)