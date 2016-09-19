---
title: "CDaoRecordset::MoveFirst"
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
ms.assetid: c01bacf3-1104-4dd4-877d-f79b3a912331
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::MoveFirst
Call this member function to make the first record in the recordset (if any) the current record.  
  
## Syntax  
  
```  
  
void MoveFirst( );  
  
```  
  
## Remarks  
 You do not have to call **MoveFirst** immediately after you open the recordset. At that time, the first record (if any) is automatically the current record.  
  
> [!CAUTION]
>  Calling any of the **Move** functions throws an exception if the recordset has no records. In general, call both `IsBOF` and `IsEOF` before a Move operation to determine whether the recordset has any records. After you call **Open** or **Requery**, call either `IsBOF` or `IsEOF`.  
  
> [!NOTE]
>  If you call any of the **Move** functions while the current record is being updated or added, the updates are lost without warning.  
  
 Use the **Move** functions to move from record to record without applying a condition. Use the Find operations to locate records in a dynaset-type or snapshot-type recordset object that satisfy a certain condition. To locate a record in a table-type recordset object, call `Seek`.  
  
 If the recordset refers to a table-type recordset, movement follows the table's current index. You can set the current index by using the Index property of the underlying DAO object. If you do not set the current index, the order of returned records is undefined.  
  
 If you call `MoveLast` on a recordset object based on a SQL query or querydef, the query is forced to completion and the recordset object is fully populated.  
  
 You cannot call the **MoveFirst** or `MovePrev` member function with a forward-only scrolling snapshot.  
  
 To move the position of the current record in a recordset object a specific number of records forward or backward, call **Move**.  
  
 For related information, see the topics "Move Method" and "MoveFirst, MoveLast, MoveNext, MovePrevious Methods" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::Move](../vs140/CDaoRecordset--Move.md)   
 [CDaoRecordset::MoveLast](../vs140/CDaoRecordset--MoveLast.md)   
 [CDaoRecordset::MoveNext](../vs140/CDaoRecordset--MoveNext.md)   
 [CDaoRecordset::MovePrev](../vs140/CDaoRecordset--MovePrev.md)