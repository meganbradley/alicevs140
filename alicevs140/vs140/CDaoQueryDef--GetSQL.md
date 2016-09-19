---
title: "CDaoQueryDef::GetSQL"
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
ms.assetid: 9869adb1-1c62-42d8-b23f-b7b2a63d33dc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetSQL
Call this member function to retrieve the SQL statement that defines the query on which the querydef is based.  
  
## Syntax  
  
```  
  
CString GetSQL( );  
  
```  
  
## Return Value  
 The SQL statement that defines the query on which the querydef is based.  
  
## Remarks  
 You will then probably parse the string for keywords, table names, and so on.  
  
 For related information, see the topics "SQL Property", "Comparison of Microsoft Jet Database Engine SQL and ANSI SQL", and "Querying a Database with SQL in Code" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::SetSQL](../vs140/CDaoQueryDef--SetSQL.md)   
 [CDaoQueryDef::GetName](../vs140/CDaoQueryDef--GetName.md)   
 [CDaoQueryDef::GetReturnsRecords](../vs140/CDaoQueryDef--GetReturnsRecords.md)   
 [CDaoQueryDef::GetODBCTimeout](../vs140/CDaoQueryDef--GetODBCTimeout.md)