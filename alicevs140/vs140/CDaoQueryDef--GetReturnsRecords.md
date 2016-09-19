---
title: "CDaoQueryDef::GetReturnsRecords"
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
ms.assetid: 6d733bf9-1700-4d50-a4eb-c07df68099a1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetReturnsRecords
Call this member function to determine whether the querydef is based on a query that returns records.  
  
## Syntax  
  
```  
  
BOOL GetReturnsRecords( );  
  
```  
  
## Return Value  
 Nonzero if the querydef is based on a query that returns records; otherwise 0.  
  
## Remarks  
 This member function is only used for SQL pass-through queries. For more information about SQL queries, see the [Execute](../vs140/CDaoQueryDef--Execute.md) member function. For more information about working with SQL pass-through queries, see the [SetReturnsRecords](../vs140/CDaoQueryDef--SetReturnsRecords.md) member function.  
  
 For related information, see the topic "ReturnsRecords Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetName](../vs140/CDaoQueryDef--GetName.md)   
 [CDaoQueryDef::GetSQL](../vs140/CDaoQueryDef--GetSQL.md)   
 [CDaoQueryDef::GetODBCTimeout](../vs140/CDaoQueryDef--GetODBCTimeout.md)