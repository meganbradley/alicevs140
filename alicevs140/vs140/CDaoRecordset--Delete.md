---
title: "CDaoRecordset::Delete"
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
ms.assetid: ceb5bcc4-4635-4c0b-8f9e-ef5848aaa7fe
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::Delete
Call this member function to delete the current record in an open dynaset-type or table-type recordset object.  
  
## Syntax  
  
```  
  
virtual void Delete( );  
  
```  
  
## Remarks  
 After a successful deletion, the recordset's field data members are set to a Null value, and you must explicitly call one of the recordset navigation member functions ([Move](../vs140/CDaoRecordset--Move.md), [Seek](../vs140/CDaoRecordset--Seek.md), [SetBookmark](../vs140/CDaoRecordset--SetBookmark.md), and so on) in order to move off the deleted record. When you delete records from a recordset, there must be a current record in the recordset before you call **Delete**; otherwise, MFC throws an exception.  
  
 **Delete** removes the current record and makes it inaccessible. Although you cannot edit or use the deleted record, it remains current. Once you move to another record, however, you cannot make the deleted record current again.  
  
> [!CAUTION]
>  The recordset must be updatable and there must be a valid record current in the recordset when you call **Delete**. For example, if you delete a record but do not scroll to a new record before you call **Delete** again, **Delete** throws a [CDaoException](../vs140/CDaoException-Class.md).  
  
 You can undelete a record if you use transactions and you call the [CDaoWorkspace::Rollback](../vs140/CDaoWorkspace--Rollback.md) member function. If the base table is the primary table in a cascade delete relationship, deleting the current record may also delete one or more records in a foreign table. For more information, see the definition "cascade delete" in DAO Help.  
  
 Unlike `AddNew` and **Edit**, a call to **Delete** is not followed by a call to **Update**.  
  
 For related information, see the topics "AddNew Method", "Edit Method", "Delete Method", "Update Method", and "Updatable Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::AddNew](../vs140/CDaoRecordset--AddNew.md)   
 [CDaoRecordset::CancelUpdate](../vs140/CDaoRecordset--CancelUpdate.md)   
 [CDaoRecordset::Edit](../vs140/CDaoRecordset--Edit.md)   
 [CDaoRecordset::Update](../vs140/CDaoRecordset--Update.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)