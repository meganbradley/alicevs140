---
title: "CDaoRecordset::Edit"
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
ms.assetid: 16a5ac51-16ef-46bc-84ef-fd38891dc0a5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::Edit
Call this member function to allow changes to the current record.  
  
## Syntax  
  
```  
  
virtual void Edit( );  
  
```  
  
## Remarks  
 Once you call the **Edit** member function, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, call **Update** to save your changes. **Edit** saves the values of the recordset's data members. If you call **Edit**, make changes, then call **Edit** again, the record's values are restored to what they were before the first **Edit** call.  
  
> [!CAUTION]
>  If you edit a record and then perform any operation that moves to another record without first calling **Update**, your changes are lost without warning. In addition, if you close the recordset or the parent database, your edited record is discarded without warning.  
  
 In some cases, you may want to update a column by making it Null (containing no data). To do so, call `SetFieldNull` with a parameter of **TRUE** to mark the field Null; this also causes the column to be updated. If you want a field to be written to the data source even though its value has not changed, call `SetFieldDirty` with a parameter of **TRUE**. This works even if the field had the value Null.  
  
 The framework marks changed field data members to ensure they will be written to the record on the data source by the DAO record field exchange (DFX) mechanism. Changing the value of a field generally sets the field dirty automatically, so you will seldom need to call [SetFieldDirty](../vs140/CDaoRecordset--SetFieldDirty.md) yourself, but you might sometimes want to ensure that columns will be explicitly updated or inserted regardless of what value is in the field data member. The DFX mechanism also employs the use of **PSEUDO NULL**. For more information, see [CDaoFieldExchange::m_nOperation](../vs140/CDaoFieldExchange--m_nOperation.md).  
  
 If the double-buffering mechanism is not being used, then changing the value of the field does not automatically set the field as dirty. In this case, it will be necessary to explicitly set the field dirty. The flag contained in [m_bCheckCacheForDirtyFields](../vs140/CDaoRecordset--m_bCheckCacheForDirtyFields.md) controls this automatic field checking.  
  
 When the recordset object is pessimistically locked in a multiuser environment, the record remains locked from the time **Edit** is used until the updating is complete. If the recordset is optimistically locked, the record is locked and compared with the pre-edited record just before it is updated in the database. If the record has changed since you called **Edit**, the **Update** operation fails and MFC throws an exception. You can change the locking mode with `SetLockingMode`.  
  
> [!NOTE]
>  Optimistic locking is always used on external database formats, such as ODBC and installable ISAM.  
  
 The current record remains current after you call **Edit**. To call **Edit**, there must be a current record. If there is no current record or if the recordset does not refer to an open table-type or dynaset-type recordset object, an exception occurs. Calling **Edit** causes a `CDaoException` to be thrown under the following conditions:  
  
-   There is no current record.  
  
-   The database or recordset is read-only.  
  
-   No fields in the record are updatable.  
  
-   The database or recordset was opened for exclusive use by another user.  
  
-   Another user has locked the page containing your record.  
  
 If the data source supports transactions, you can make the **Edit** call part of a transaction. Note that you should call `CDaoWorkspace::BeginTrans` before calling **Edit** and after the recordset has been opened. Also note that calling `CDaoWorkspace::CommitTrans` is not a substitute for calling **Update** to complete the **Edit** operation. For more information about transactions, see class `CDaoWorkspace`.  
  
 For related information, see the topics "AddNew Method", "Edit Method", "Delete Method", "Update Method", and "Updatable Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::AddNew](../vs140/CDaoRecordset--AddNew.md)   
 [CDaoRecordset::CancelUpdate](../vs140/CDaoRecordset--CancelUpdate.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)   
 [CDaoRecordset::Delete](../vs140/CDaoRecordset--Delete.md)   
 [CDaoRecordset::Update](../vs140/CDaoRecordset--Update.md)