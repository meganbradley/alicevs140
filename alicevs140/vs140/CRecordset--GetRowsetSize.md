---
title: "CRecordset::GetRowsetSize"
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
ms.assetid: 4c886140-d98b-4035-b3c5-5415cdffcb9f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetRowsetSize
Obtains the current setting for the number of rows you wish to retrieve during a given fetch.  
  
## Syntax  
  
```  
  
DWORD GetRowsetSize( ) const;  
  
```  
  
## Return Value  
 The number of rows to retrieve during a given fetch.  
  
## Remarks  
 If you are using bulk row fetching, the default rowset size when the recordset is opened is 25; otherwise, it is 1.  
  
 To implement bulk row fetching, you must specify the `CRecordset::useMultiRowFetch` option in the `dwOptions` parameter of the [Open](../vs140/CRecordset--Open.md) member function. To change the setting for the rowset size, call [SetRowsetSize](../vs140/CRecordset--SetRowsetSize.md).  
  
 For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Open](../vs140/CRecordset--Open.md)   
 [CRecordset::SetRowsetSize](../vs140/CRecordset--SetRowsetSize.md)   
 [CRecordset::CheckRowsetError](../vs140/CRecordset--CheckRowsetError.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)