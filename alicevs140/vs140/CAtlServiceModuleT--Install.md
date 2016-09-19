---
title: "CAtlServiceModuleT::Install"
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
ms.assetid: 9bbbf339-d387-4ceb-9c5b-fd8d9db19a63
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::Install
Installs and creates the service.  
  
## Syntax  
  
```  
  
BOOL Install( ) throw( );  
  
```  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 Installs the service into the Service Control Manager (SCM) database and then creates the service object. If the service could not be created, a message box is displayed and the method returns FALSE.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)   
 [CreateService](http://msdn.microsoft.com/library/windows/desktop/ms682450)   
 [CAtlServiceModuleT::Uninstall](../vs140/CAtlServiceModuleT--Uninstall.md)