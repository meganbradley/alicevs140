---
title: "CDaoQueryDef::SetReturnsRecords"
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
ms.assetid: 9feab1fb-d3f0-40d9-ae99-9955aceefd8a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoQueryDef::SetReturnsRecords
Call this member function as part of the process of setting up a SQL pass-through query to an external database.  
  
## Syntax  
  
```  
  
      void SetReturnsRecords(   
   BOOL bReturnsRecords    
);  
```  
  
#### Parameters  
 *bReturnsRecords*  
 Pass **TRUE** if the query on an external database returns records; otherwise, **FALSE**.  
  
## Remarks  
 In such a case, you must create the querydef and set its properties using other `CDaoQueryDef` member functions. For a description of external databases, see [SetConnect](../vs140/CDaoQueryDef--SetConnect.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoQueryDef::GetReturnsRecords](../vs140/CDaoQueryDef--GetReturnsRecords.md)   
 [CDaoQueryDef::SetName](../vs140/CDaoQueryDef--SetName.md)   
 [CDaoQueryDef::SetSQL](../vs140/CDaoQueryDef--SetSQL.md)   
 [CDaoQueryDef::SetConnect](../vs140/CDaoQueryDef--SetConnect.md)   
 [CDaoQueryDef::SetODBCTimeout](../vs140/CDaoQueryDef--SetODBCTimeout.md)