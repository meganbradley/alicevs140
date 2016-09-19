---
title: "CAtlServiceModuleT::ServiceMain"
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
ms.assetid: 1675d69e-2de1-46da-bc34-0d7881d7cf39
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::ServiceMain
This method is called by the Service Control Manager.  
  
## Syntax  
  
```  
  
      void ServiceMain(  
   DWORD dwArgc,  
   LPTSTR* lpszArgv   
) throw( );  
```  
  
#### Parameters  
 *dwArgc*  
 The argc argument.  
  
 *lpszArgv*  
 The argv argument.  
  
## Remarks  
 The Service Control Manager (SCM) calls `ServiceMain` when you open the Services application in the Control Panel, select the service, and click Start.  
  
 After the SCM calls `ServiceMain`, a service must give the SCM a handler function. This function lets the SCM obtain the service's status and pass specific instructions (such as pausing or stopping). Subsequently, [CAtlServiceModuleT::Run](../vs140/CAtlServiceModuleT--Run.md) is called to perform the main work of the service. **Run** continues to execute until the service is stopped.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)