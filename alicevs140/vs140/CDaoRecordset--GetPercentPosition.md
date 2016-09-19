---
title: "CDaoRecordset::GetPercentPosition"
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
ms.assetid: 2a2b9c2b-e531-42b1-b41a-1ad52c5ccb46
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetPercentPosition
When working with a dynaset-type or snapshot-type recordset, if you call `GetPercentPosition` before fully populating the recordset, the amount of movement is relative to the number of records accessed as indicated by calling [GetRecordCount](../vs140/CDaoRecordset--GetRecordCount.md).  
  
## Syntax  
  
```  
  
float GetPercentPosition( );  
  
```  
  
## Return Value  
 A number between 0 and 100 that indicates the approximate location of the current record in the recordset object based on a percentage of the records in the recordset.  
  
## Remarks  
 You can move to the last record by calling [MoveLast](../vs140/CDaoRecordset--MoveLast.md) to complete the population of all recordsets, but this may take a significant amount of time.  
  
 You can call `GetPercentPosition` on all three types of recordset objects, including tables without indexes. However, you cannot call `GetPercentPosition` on forward-only scrolling snapshots, or on a recordset opened from a pass-through query against an external database. If there is no current record, or he current record has been deleted, a `CDaoException` is thrown.  
  
 For related information, see the topic "PercentPosition Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::SetPercentPosition](../vs140/CDaoRecordset--SetPercentPosition.md)