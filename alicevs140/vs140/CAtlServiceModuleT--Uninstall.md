---
title: "CAtlServiceModuleT::Uninstall"
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
ms.assetid: 47faa555-5358-4c4f-8bce-88e3bea016be
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::Uninstall
Stops and removes the service.  
  
## Syntax  
  
```  
  
BOOL Uninstall( ) throw( );  
  
```  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 Stops the service from running and removes it from the Service Control Manager database.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)   
 [CAtlServiceModuleT::Install](../vs140/CAtlServiceModuleT--Install.md)