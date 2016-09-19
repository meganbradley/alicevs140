---
title: "CDataRecoveryHandler::SetSaveDocumentInfoOnIdle"
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
ms.assetid: 17beb7b3-2215-465e-a1f5-c0487a10a680
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::SetSaveDocumentInfoOnIdle
Sets whether the `CDataRecoveryHandler` saves the open document information to the Windows registry during the current idle cycle.  
  
## Syntax  
  
```  
virtual void SetSaveDocumentInfoOnIdle(  
   BOOL bSaveOnIdle  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `bSaveOnIdle`|`TRUE` to save document information during the current idle cycle; `FALSE to not perform a save`.|  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::GetSaveDocumentInfoOnIdle](../vs140/CDataRecoveryHandler--GetSaveDocumentInfoOnIdle.md)