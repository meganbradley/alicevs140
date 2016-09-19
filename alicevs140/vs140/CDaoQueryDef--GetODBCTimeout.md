---
title: "CDaoQueryDef::GetODBCTimeout"
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
ms.assetid: e0595012-631c-4837-a768-3c51cd0ba51d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetODBCTimeout
Call this member function to retrieve the current time limit before a query to an ODBC data source times out.  
  
## Syntax  
  
```  
  
short GetODBCTimeout( );  
  
```  
  
## Return Value  
 The number of seconds before a query times out.  
  
## Remarks  
 For information about this time limit, see the topic "ODBCTimeout Property" in DAO Help.  
  
> [!TIP]
>  The preferred way to work with ODBC tables is to attach them to a Microsoft Jet (.MDB) database. For more information, see the topic "Accessing External Databases with DAO" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::SetODBCTimeout](../vs140/CDaoQueryDef--SetODBCTimeout.md)   
 [CDaoQueryDef::GetName](../vs140/CDaoQueryDef--GetName.md)   
 [CDaoQueryDef::GetSQL](../vs140/CDaoQueryDef--GetSQL.md)   
 [CDaoQueryDef::GetReturnsRecords](../vs140/CDaoQueryDef--GetReturnsRecords.md)