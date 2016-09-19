---
title: "CDaoRecordset::MoveNext"
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
ms.assetid: 55559267-17ea-4ef8-b368-40c086ac23f4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::MoveNext
Call this member function to make the next record in the recordset the current record.  
  
## Syntax  
  
```  
  
void MoveNext( );  
  
```  
  
## Remarks  
 It is recommended that you call `IsBOF` before you attempt to move to the previous record. A call to `MovePrev` will throw a `CDaoException` if `IsBOF` returns nonzero, indicating either that you have already scrolled before the first record or that no records were selected by the recordset.  
  
> [!CAUTION]
>  Calling any of the **Move** functions throws an exception if the recordset has no records. In general, call both `IsBOF` and `IsEOF` before a Move operation to determine whether the recordset has any records. After you call **Open** or **Requery**, call either `IsBOF` or `IsEOF`.  
  
> [!NOTE]
>  If you call any of the **Move** functions while the current record is being updated or added, the updates are lost without warning.  
  
 Use the **Move** functions to move from record to record without applying a condition. Use the Find operations to locate records in a dynaset-type or snapshot-type recordset object that satisfy a certain condition. To locate a record in a table-type recordset object, call `Seek`.  
  
 If the recordset refers to a table-type recordset, movement follows the table's current index. You can set the current index by using the Index property of the underlying DAO object. If you do not set the current index, the order of returned records is undefined.  
  
 To move the position of the current record in a recordset object a specific number of records forward or backward, call **Move**.  
  
 For related information, see the topics "Move Method" and "MoveFirst, MoveLast, MoveNext, MovePrevious Methods" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::Move](../vs140/CDaoRecordset--Move.md)   
 [CDaoRecordset::MoveFirst](../vs140/CDaoRecordset--MoveFirst.md)   
 [CDaoRecordset::MoveLast](../vs140/CDaoRecordset--MoveLast.md)   
 [CDaoRecordset::MovePrev](../vs140/CDaoRecordset--MovePrev.md)