---
title: "CDaoQueryDef::GetName"
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
ms.assetid: 29fa5581-12ff-491b-91e2-3cbf99fa3577
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::GetName
Call this member function to retrieve the name of the query represented by the querydef.  
  
## Syntax  
  
```  
  
CString GetName( );  
  
```  
  
## Return Value  
 The name of the query.  
  
## Remarks  
 Querydef names are unique user-defined names. For more information about querydef names, see the topic "Name Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::SetName](../vs140/CDaoQueryDef--SetName.md)   
 [CDaoQueryDef::GetSQL](../vs140/CDaoQueryDef--GetSQL.md)   
 [CDaoQueryDef::GetReturnsRecords](../vs140/CDaoQueryDef--GetReturnsRecords.md)   
 [CDaoQueryDef::GetODBCTimeout](../vs140/CDaoQueryDef--GetODBCTimeout.md)