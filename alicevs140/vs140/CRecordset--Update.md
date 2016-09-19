---
title: "CRecordset::Update"
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
ms.assetid: 2ed347a4-c7a8-4dad-b84d-cf85f1959eb6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::Update
Completes an `AddNew` or **Edit** operation by saving the new or edited data on the data source.  
  
## Syntax  
  
```  
  
virtual BOOL Update( );  
  
```  
  
## Return Value  
 Nonzero if one record was successfully updated; otherwise 0 if no columns have changed. If no records were updated, or if more than one record was updated, an exception is thrown. An exception is also thrown for any other failure on the data source.  
  
## Remarks  
 Call this member function after a call to the [AddNew](../vs140/CRecordset--AddNew.md) or [Edit](../vs140/CRecordset--Edit.md) member function. This call is required to complete the `AddNew` or **Edit** operation.  
  
> [!NOTE]
>  If you have implemented bulk row fetching, you cannot call **Update**. This will result in a failed assertion. Although class `CRecordset` does not provide a mechanism for updating bulk rows of data, you can write your own functions by using the ODBC API function **SQLSetPos**. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 Both `AddNew` and **Edit** prepare an edit buffer in which the added or edited data is placed for saving to the data source. **Update** saves the data. Only those fields marked or detected as changed are updated.  
  
 If the data source supports transactions, you can make the **Update** call (and its corresponding `AddNew` or **Edit** call) part of a transaction. For more information about transactions, see the article [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
> [!CAUTION]
>  If you call **Update** without first calling either `AddNew` or **Edit**, **Update** throws a `CDBException`. If you call `AddNew` or **Edit**, you must call **Update** before you call a **Move** operation or before you close either the recordset or the data source connection. Otherwise, your changes are lost without notification.  
  
 For details on handling **Update** failures, see the article [Recordset: How Recordsets Update Records (ODBC)](../vs140/Recordset--How-Recordsets-Update-Records--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\***.  
  
## Example  
 See the article [Transaction: Performing a Transaction in a Recordset (ODBC)](../vs140/Transaction--Performing-a-Transaction-in-a-Recordset--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Edit](../vs140/CRecordset--Edit.md)   
 [CRecordset::AddNew](../vs140/CRecordset--AddNew.md)   
 [CRecordset::SetFieldDirty](../vs140/CRecordset--SetFieldDirty.md)   
 [CDBException Class](../vs140/CDBException-Class.md)