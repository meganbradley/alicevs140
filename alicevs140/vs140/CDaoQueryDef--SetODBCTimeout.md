---
title: "CDaoQueryDef::SetODBCTimeout"
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
ms.assetid: 1e7efa5c-54c4-4670-b868-091c1e988cd5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::SetODBCTimeout
Call this member function to set the time limit before a query to an ODBC data source times out.  
  
## Syntax  
  
```  
  
      void SetODBCTimeout(   
   short nODBCTimeout    
);  
```  
  
#### Parameters  
 *nODBCTimeout*  
 The number of seconds before a query times out.  
  
## Remarks  
 This member function lets you override the default number of seconds before subsequent operations on the connected data source "time out." An operation might time out due to network access problems, excessive query processing time, and so on. Call `SetODBCTimeout` prior to executing a query with this querydef if you want to change the query timeout value. (As ODBC reuses connections, the timeout value is the same for all clients on the same connection.)  
  
 The default value for query timeouts is 60 seconds.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetODBCTimeout](../vs140/CDaoQueryDef--GetODBCTimeout.md)   
 [CDaoQueryDef::SetName](../vs140/CDaoQueryDef--SetName.md)   
 [CDaoQueryDef::SetSQL](../vs140/CDaoQueryDef--SetSQL.md)   
 [CDaoQueryDef::SetConnect](../vs140/CDaoQueryDef--SetConnect.md)   
 [CDaoQueryDef::SetReturnsRecords](../vs140/CDaoQueryDef--SetReturnsRecords.md)