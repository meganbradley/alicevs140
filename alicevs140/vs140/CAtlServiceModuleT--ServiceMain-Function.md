---
title: "CAtlServiceModuleT::ServiceMain Function"
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
ms.assetid: f21408c1-1919-4dec-88d8-bf5b39ac9808
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::ServiceMain Function
The service control manager (SCM) calls `ServiceMain` when you open the Services Control Panel application, select the service, and click **Start**.  
  
 After the SCM calls `ServiceMain`, a service must give the SCM a handler function. This function lets the SCM obtain the service's status and pass specific instructions (such as pausing or stopping). The SCM gets this function when the service passes **_Handler** to the Win32 API function, [RegisterServiceCtrlHandler](http://msdn.microsoft.com/library/windows/desktop/ms685054). (**_Handler** is a static member function that calls the non-static member function [Handler](../vs140/CAtlServiceModuleT--Handler-Function.md).)  
  
 At startup, a service should also inform the SCM of its current status. It does this by passing **SERVICE_START_PENDING** to the Win32 API function, [SetServiceStatus](http://msdn.microsoft.com/library/windows/desktop/ms686241).  
  
 `ServiceMain` then calls `CAtlExeModuleT::InitializeCom`, which calls the Win32 API function [CoInitializeEx](http://msdn.microsoft.com/library/windows/desktop/ms695279). By default, `InitializeCom` passes the **COINIT_MULTITHREADED** flag to the function. This flag indicates that the program is to be a free-threaded server.  
  
 Now, `CAtlServiceModuleT::Run` is called to perform the main work of the service. **Run** continues to execute until the service is stopped.  
  
## See Also  
 [Services](../vs140/ATL-Services.md)   
 [CAtlServiceModuleT::ServiceMain](../vs140/CAtlServiceModuleT--ServiceMain.md)