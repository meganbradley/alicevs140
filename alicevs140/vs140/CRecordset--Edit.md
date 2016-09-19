---
title: "CRecordset::Edit"
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
ms.assetid: 23e34175-5af8-4b65-9551-d6983d718ac7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::Edit
Allows changes to the current record.  
  
## Syntax  
  
```  
  
virtual void Edit( );  
  
```  
  
## Remarks  
 After you call **Edit**, you can change the field data members by directly resetting their values. The operation is completed when you subsequently call the [Update](../vs140/CRecordset--Update.md) member function to save your changes on the data source.  
  
> [!NOTE]
>  If you have implemented bulk row fetching, you cannot call **Edit**. This will result in a failed assertion. Although class `CRecordset` does not provide a mechanism for updating bulk rows of data, you can write your own functions by using the ODBC API function **SQLSetPos**. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 **Edit** saves the values of the recordset's data members. If you call **Edit**, make changes, then call **Edit** again, the record's values are restored to what they were before the first **Edit** call.  
  
 In some cases, you may want to update a column by making it Null (containing no data). To do so, call [SetFieldNull](../vs140/CRecordset--SetFieldNull.md) with a parameter of **TRUE** to mark the field Null; this also causes the column to be updated. If you want a field to be written to the data source even though its value has not changed, call [SetFieldDirty](../vs140/CRecordset--SetFieldDirty.md) with a parameter of **TRUE**. This works even if the field had the value Null.  
  
 If the data source supports transactions, you can make the **Edit** call part of a transaction. Note that you should call [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md) before calling **Edit** and after the recordset has been opened. Also note that calling [CDatabase::CommitTrans](../vs140/CDatabase--CommitTrans.md) is not a substitute for calling **Update** to complete the **Edit** operation. For more information about transactions, see class [CDatabase](../vs140/CDatabase-Class.md).  
  
 Depending on the current locking mode, the record being updated may be locked by **Edit** until you call **Update** or scroll to another record, or it may be locked only during the **Edit** call. You can change the locking mode with [SetLockingMode](../vs140/CRecordset--SetLockingMode.md).  
  
 The previous value of the current record is restored if you scroll to a new record before calling **Update**. A `CDBException` is thrown if you call **Edit** for a recordset that cannot be updated or if there is no current record.  
  
 For more information, see the articles [Transaction (ODBC)](../vs140/Transaction--ODBC-.md) and [Recordset: Locking Records (ODBC)](../vs140/Recordset--Locking-Records--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Example  
 [!CODE [NVC_MFCDatabase#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#20)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Update](../vs140/CRecordset--Update.md)   
 [CRecordset::AddNew](../vs140/CRecordset--AddNew.md)   
 [CRecordset::Delete](../vs140/CRecordset--Delete.md)   
 [CRecordset::SetFieldDirty](../vs140/CRecordset--SetFieldDirty.md)   
 [CRecordset::SetFieldNull](../vs140/CRecordset--SetFieldNull.md)   
 [CRecordset::CanUpdate](../vs140/CRecordset--CanUpdate.md)   
 [CRecordset::CanTransact](../vs140/CRecordset--CanTransact.md)   
 [CRecordset::SetLockingMode](../vs140/CRecordset--SetLockingMode.md)