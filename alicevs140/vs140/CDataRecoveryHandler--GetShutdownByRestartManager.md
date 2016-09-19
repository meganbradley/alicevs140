---
title: "CDataRecoveryHandler::GetShutdownByRestartManager"
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
ms.assetid: 9860f05a-6b82-4690-9c24-8b1dd8a129c5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::GetShutdownByRestartManager
Indicates whether the restart manager caused the application to exit.  
  
## Syntax  
  
```  
virtual BOOL GetShutdownByRestartManager() const;  
```  
  
## Return Value  
 `TRUE` indicates the restart manager caused the application to exit; `FALSE` indicates it did not.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::SetShutdownByRestartManager](../vs140/CDataRecoveryHandler--SetShutdownByRestartManager.md)