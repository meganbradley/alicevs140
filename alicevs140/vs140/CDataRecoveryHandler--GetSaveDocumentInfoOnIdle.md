---
title: "CDataRecoveryHandler::GetSaveDocumentInfoOnIdle"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 3ceb02bd-767f-4961-a652-3bbd2bbcb00f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::GetSaveDocumentInfoOnIdle
Indicates whether the `CDataRecoveryHandler` performs an autosave on the current idle loop.  
  
## Syntax  
  
```  
virtual BOOL GetSaveDocumentInfoOnIdle() const;  
```  
  
## Return Value  
 `TRUE` indicates the `CDataRecoveryHandler` autosaves on the current idle loop; `FALSE` indicates it does not.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::SetSaveDocumentInfoOnIdle](../vs140/CDataRecoveryHandler--SetSaveDocumentInfoOnIdle.md)