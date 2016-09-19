---
title: "CDaoWorkspace::GetWorkspaceCount"
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
ms.assetid: b3b81088-d730-4a3e-837e-2d769f3a4363
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoWorkspace::GetWorkspaceCount
Call this member function to retrieve the number of DAO workspace objects in the database engine's Workspaces collection.  
  
## Syntax  
  
```  
  
short GetWorkspaceCount( );  
  
```  
  
## Return Value  
 The number of open workspaces in the Workspaces collection.  
  
## Remarks  
 This count does not include any open workspaces not appended to the collection. `GetWorkspaceCount` is useful if you need to loop through all defined workspaces in the Workspaces collection. To obtain information about a given workspace in the collection, see [GetWorkspaceInfo](../vs140/CDaoWorkspace--GetWorkspaceInfo.md). Typical usage is to call `GetWorkspaceCount` for the number of open workspaces, then use that number as a loop index for repeated calls to `GetWorkspaceInfo`.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoWorkspace Class](../vs140/CDaoWorkspace-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)