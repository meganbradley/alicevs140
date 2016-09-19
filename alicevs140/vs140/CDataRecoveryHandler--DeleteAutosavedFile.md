---
title: "CDataRecoveryHandler::DeleteAutosavedFile"
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
ms.assetid: eb5c233e-238b-410b-b5ba-034a7e1aed43
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataRecoveryHandler::DeleteAutosavedFile
Deletes the specified autosaved file.  
  
## Syntax  
  
```  
virtual BOOL DeleteAutosavedFile(  
   const CString &strAutosavedFile  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `strAutosavedFile`|A string that contains the autosaved file name.|  
  
## Return Value  
 The default implementation always return `TRUE`.  
  
## Remarks  
 If this method cannot delete the autosaved file, it saves the name of the file in a list. The destructor for the `CDataRecoveryHandler` tries to delete each autosaved file specified in that list.  
  
## Requirements  
 **Header:** afxdatarecovery.h  
  
## See Also  
 [CDataRecoveryHandler Class](../vs140/CDataRecoveryHandler-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDataRecoveryHandler::DeleteAllAutosavedFiles](../vs140/CDataRecoveryHandler--DeleteAllAutosavedFiles.md)