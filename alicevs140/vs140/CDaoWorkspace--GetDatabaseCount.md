---
title: "CDaoWorkspace::GetDatabaseCount"
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
ms.assetid: 622fdd73-42b7-4308-a039-61c38826a08c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::GetDatabaseCount
Call this member function to retrieve the number of DAO database objects in the workspace's Databases collection — the number of open databases in the workspace.  
  
## Syntax  
  
```  
  
short GetDatabaseCount( );  
  
```  
  
## Return Value  
 The number of open databases in the workspace.  
  
## Remarks  
 `GetDatabaseCount` is useful if you need to loop through all defined databases in the workspace's Databases collection. To obtain information about a given database in the collection, see [GetDatabaseInfo](../vs140/CDaoWorkspace--GetDatabaseInfo.md). Typical usage is to call `GetDatabaseCount` for the number of open databases, then use that number as a loop index for repeated calls to `GetDatabaseInfo`.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)