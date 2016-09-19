---
title: "Recordset: Locking Records (ODBC)"
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
ms.topic: article
ms.assetid: 8fe8fcfe-b55a-41a8-9136-94a7cd1e4806
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recordset: Locking Records (ODBC)
This topic applies to the MFC ODBC classes.  
  
 This topic explains:  
  
-   [The kinds of record locking available](#_core_record.2d.locking_modes).  
  
-   [How to lock records in your recordset during updates](#_core_locking_records_in_your_recordset).  
  
 When you use a recordset to update a record on the data source, your application can lock the record so no other user can update the record at the same time. The state of a record updated by two users at the same time is undefined unless the system can guarantee that two users cannot update a record simultaneously.  
  
> [!NOTE]
>  This topic applies to objects derived from `CRecordset` in which bulk row fetching has not been implemented. If you have implemented bulk row fetching, some of the information does not apply. For example, you cannot call the **Edit** and **Update** member functions. For more information about bulk row fetching, see [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
##  <a name="_core_record.2d.locking_modes"></a> Record-Locking Modes  
 The database classes provide two [record-locking modes](../vs140/CRecordset--SetLockingMode.md):  
  
-   Optimistic locking (the default)  
  
-   Pessimistic locking  
  
 Updating a record occurs in three steps:  
  
1.  You begin the operation by calling the [Edit](../vs140/CRecordset--Edit.md) member function.  
  
2.  You change the appropriate fields of the current record.  
  
3.  You end the operation — and normally commit the update — by calling the [Update](../vs140/CRecordset--Update.md) member function.  
  
 Optimistic locking locks the record on the data source only during the **Update** call. If you use optimistic locking in a multiuser environment, the application should handle an **Update** failure condition. Pessimistic locking locks the record as soon as you call **Edit** and does not release it until you call **Update** (failures are indicated through the `CDBException` mechanism, not by a value of **FALSE** returned by **Update**). Pessimistic locking has a potential performance penalty for other users, because concurrent access to the same record might have to wait until completion of your application's **Update** process.  
  
##  <a name="_core_locking_records_in_your_recordset"></a> Locking Records in Your Recordset  
 If you want to change a recordset object's [locking mode](#_core_record.2d.locking_modes) from the default, you must change the mode before you call **Edit**.  
  
#### To change the current locking mode for your recordset  
  
1.  Call the [SetLockingMode](../vs140/CRecordset--SetLockingMode.md) member function, specifying either **CRecordset::pessimistic** or **CRecordset::optimistic**.  
  
 The new locking mode remains in effect until you change it again or the recordset is closed.  
  
> [!NOTE]
>  Relatively few ODBC drivers currently support pessimistic locking.  
  
## See Also  
 [Recordset (ODBC)](../vs140/Recordset--ODBC-.md)   
 [Recordset: Performing a Join (ODBC)](../vs140/Recordset--Performing-a-Join--ODBC-.md)   
 [Recordset: Adding, Updating, and Deleting Records (ODBC)](../vs140/Recordset--Adding--Updating--and-Deleting-Records--ODBC-.md)