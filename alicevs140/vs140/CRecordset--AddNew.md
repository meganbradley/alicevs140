---
title: "CRecordset::AddNew"
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
ms.assetid: 2db92826-51bc-46c0-924e-22986554bb1b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::AddNew
Prepares for adding a new record to the table.  
  
## Syntax  
  
```  
  
virtual void AddNew( );  
  
```  
  
## Remarks  
 You must call the [Requery](../vs140/CRecordset--Requery.md) member function to see the newly added record. The record's fields are initially Null. (In database terminology, Null means "having no value" and is not the same as **NULL** in C++.) To complete the operation, you must call the [Update](../vs140/CRecordset--Update.md) member function. **Update** saves your changes to the data source.  
  
> [!NOTE]
>  If you have implemented bulk row fetching, you cannot call `AddNew`. This will result in a failed assertion. Although class `CRecordset` does not provide a mechanism for updating bulk rows of data, you can write your own functions by using the ODBC API function **SQLSetPos**. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 `AddNew` prepares a new, empty record using the recordset's field data members. After you call `AddNew`, set the values you want in the recordset's field data members. (You do not have to call the [Edit](../vs140/CRecordset--Edit.md) member function for this purpose; use **Edit** only for existing records.) When you subsequently call **Update**, changed values in the field data members are saved on the data source.  
  
> [!CAUTION]
>  If you scroll to a new record before you call **Update**, the new record is lost, and no warning is given.  
  
 If the data source supports transactions, you can make your `AddNew` call part of a transaction. For more information about transactions, see class [CDatabase](../vs140/CDatabase-Class.md). Note that you should call [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md) before calling `AddNew`.  
  
> [!NOTE]
>  For dynasets, new records are added to the recordset as the last record. Added records are not added to snapshots; you must call **Requery** to refresh the recordset.  
  
 It is illegal to call `AddNew` for a recordset whose **Open** member function has not been called. A `CDBException` is thrown if you call `AddNew` for a recordset that cannot be appended to. You can determine whether the recordset is updatable by calling [CanAppend](../vs140/CRecordset--CanAppend.md).  
  
 For more information, see the following articles: [Recordset: How Recordsets Update Records (ODBC)](../vs140/Recordset--How-Recordsets-Update-Records--ODBC-.md), [Recordset: Adding, Updating, and Deleting Records (ODBC)](../vs140/Recordset--Adding--Updating--and-Deleting-Records--ODBC-.md), and [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
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
 [CRecordset::Delete](../vs140/CRecordset--Delete.md)   
 [CRecordset::Update](../vs140/CRecordset--Update.md)   
 [CRecordset::Requery](../vs140/CRecordset--Requery.md)   
 [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md)   
 [CDBException Class](../vs140/CDBException-Class.md)