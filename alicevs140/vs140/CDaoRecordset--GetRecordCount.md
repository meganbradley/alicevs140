---
title: "CDaoRecordset::GetRecordCount"
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
ms.assetid: 60b8aea9-1a47-4a83-af61-514c075ae25d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetRecordCount
Call this member function to find out how many records in a recordset have been accessed.  
  
## Syntax  
  
```  
  
long GetRecordCount( );  
  
```  
  
## Return Value  
 Returns the number of records accessed in a recordset object.  
  
## Remarks  
 `GetRecordCount` does not indicate how many records are contained in a dynaset-type or snapshot-type recordset until all records have been accessed. This member function call may take a significant amount of time to complete.  
  
 Once the last record has been accessed, the return value indicates the total number of undeleted records in the recordset. To force the last record to be accessed, call the `MoveLast` or `FindLast` member function for the recordset. You can also use a SQL Count to determine the approximate number of records your query will return.  
  
 As your application deletes records in a dynaset-type recordset, the return value of `GetRecordCount` decreases. However, records deleted by other users are not reflected by `GetRecordCount` until the current record is positioned to a deleted record. If you execute a transaction that affects the record count and subsequently roll back the transaction, `GetRecordCount` will not reflect the actual number of remaining records.  
  
 The value of `GetRecordCount` from a snapshot-type recordset is not affected by changes in the underlying tables.  
  
 The value of `GetRecordCount` from a table-type recordset reflects the approximate number of records in the table and is affected immediately as table records are added and deleted.  
  
 A recordset with no records returns a value of 0. When working with attached tables or ODBC databases, `GetRecordCount` always returns – 1. Calling the **Requery** member function on a recordset resets the value of `GetRecordCount` just as if the query were re-executed.  
  
 For related information, see the topic "RecordCount Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetFieldCount](../vs140/CDaoRecordset--GetFieldCount.md)   
 [CDaoRecordset::GetFieldInfo](../vs140/CDaoRecordset--GetFieldInfo.md)   
 [CDaoRecordset::GetIndexCount](../vs140/CDaoRecordset--GetIndexCount.md)   
 [CDaoRecordset::GetIndexInfo](../vs140/CDaoRecordset--GetIndexInfo.md)