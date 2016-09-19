---
title: "CDataRecoveryHandler::Initialize"
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
ms.assetid: d31df588-3806-4345-b906-828f7e2b586e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::Initialize
Initializes the `CDataRecoveryHandler`.  
  
## Syntax  
  
```  
virtual BOOL Initialize();  
```  
  
## Return Value  
 `TRUE` if the initialization is successful; otherwise `FALSE`.  
  
## Remarks  
 The initialization process loads the path for storing autosave files from the registry. If the `Initialize` method cannot find this directory or if the path is `NULL`, `Initialize` fails and returns `FALSE`.  
  
 Use [CDataRecoveryHandler::SetAutosavePath](../vs140/CDataRecoveryHandler--SetAutosavePath.md) to change the autosave path after your application initializes the `CDataRecoveryHandler`.  
  
 The `Initialize` method also starts a timer to monitor when the next autosave occurs. Use [CDataRecoveryHandler::SetAutosaveInterval](../vs140/CDataRecoveryHandler--SetAutosaveInterval.md) to change the autosave interval after your application initializes the `CDataRecoveryHandler`.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::SetAutosavePath](../vs140/CDataRecoveryHandler--SetAutosavePath.md)   
 [CDataRecoveryHandler::SetAutosaveInterval](../vs140/CDataRecoveryHandler--SetAutosaveInterval.md)