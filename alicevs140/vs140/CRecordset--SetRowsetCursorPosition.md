---
title: "CRecordset::SetRowsetCursorPosition"
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
ms.assetid: dd4bad32-e908-4c22-b96f-5e9a7a988336
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetRowsetCursorPosition
Moves the cursor to a row within the current rowset.  
  
## Syntax  
  
```  
  
      void SetRowsetCursorPosition(  
   WORD wRow,  
   WORD wLockType = SQL_LOCK_NO_CHANGE   
);  
```  
  
#### Parameters  
 `wRow`  
 The one-based position of a row in the current rowset. This value can range from 1 to the size of the rowset.  
  
 `wLockType`  
 Value indicating how to lock the row after it has been refreshed. For details, see Remarks.  
  
## Remarks  
 When implementing bulk row fetching, records are retrieved by rowsets, where the first record in the fetched rowset is the current record. In order to make another record within the rowset the current record, call `SetRowsetCursorPosition`. For example, you can combine `SetRowsetCursorPosition` with the [GetFieldValue](../vs140/CRecordset--GetFieldValue.md) member function to dynamically retrieve the data from any record of your recordset.  
  
 To use `SetRowsetCursorPosition`, you must have implemented bulk row fetching by specifying the `CRecordset::useMultiRowFetch` option of the `dwOptions` parameter in the [Open](../vs140/CRecordset--Open.md) member function.  
  
 `SetRowsetCursorPosition` calls the ODBC API function **SQLSetPos**. The `wLockType` parameter specifies the lock state of the row after **SQLSetPos** has executed. The following table describes the possible values for `wLockTyp`e.  
  
|wLockType|Description|  
|---------------|-----------------|  
|`SQL_LOCK_NO_CHANGE` (the default value)|The driver or data source ensures that the row is in the same locked or unlocked state as it was before `SetRowsetCursorPosition` was called.|  
|`SQL_LOCK_EXCLUSIVE`|The driver or data source locks the row exclusively. Not all data sources support this type of lock.|  
|`SQL_LOCK_UNLOCK`|The driver or data source unlocks the row. Not all data sources support this type of lock.|  
  
 For more information about **SQLSetPos**, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::RefreshRowset](../vs140/CRecordset--RefreshRowset.md)   
 [CRecordset::SetRowsetSize](../vs140/CRecordset--SetRowsetSize.md)