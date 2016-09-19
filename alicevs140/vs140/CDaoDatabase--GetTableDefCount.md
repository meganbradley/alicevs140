---
title: "CDaoDatabase::GetTableDefCount"
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
ms.assetid: 98c70230-e447-448b-b99c-4451f8179389
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetTableDefCount
Call this member function to retrieve the number of tables defined in the database.  
  
## Syntax  
  
```  
  
short GetTableDefCount( );  
  
```  
  
## Return Value  
 The number of tabledefs defined in the database.  
  
## Remarks  
 `GetTableDefCount` is useful if you need to loop through all tabledefs in the database's TableDefs collection. To obtain information about a given table in the collection, see [GetTableDefInfo](../vs140/CDaoDatabase--GetTableDefInfo.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)