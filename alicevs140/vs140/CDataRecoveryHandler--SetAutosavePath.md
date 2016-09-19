---
title: "CDataRecoveryHandler::SetAutosavePath"
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
ms.assetid: 150126e0-7a61-4df5-a9ca-b4d45ba22cd6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::SetAutosavePath
Sets the directory where autosaved files are stored.  
  
## Syntax  
  
```  
virtual void SetAutosavePath(  
   const CString &strAutosavePath  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `strAutosavePath`|The path where autosave files are stored.|  
  
## Remarks  
 Changing the autosave directory does not move currently autosaved files.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::GetAutosavePath](../vs140/CDataRecoveryHandler--GetAutosavePath.md)