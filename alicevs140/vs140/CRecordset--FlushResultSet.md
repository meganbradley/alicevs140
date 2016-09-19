---
title: "CRecordset::FlushResultSet"
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
ms.assetid: 21502f57-e174-4937-b775-9cc07b70cb91
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::FlushResultSet
Retrieves the next result set of a predefined query (stored procedure), if there are multiple result sets.  
  
## Syntax  
  
```  
  
BOOL FlushResultSet( );  
  
```  
  
## Return Value  
 Nonzero if there are more result sets to be retrieved; otherwise 0.  
  
## Remarks  
 You should call `FlushResultSet` only when you are completely finished with the cursor on the current result set. Note that when you retrieve the next result set by calling `FlushResultSet`, your cursor is not valid on that result set; you should call the [MoveNext](../vs140/CRecordset--MoveNext.md) member function after calling `FlushResultSet`.  
  
 If a predefined query uses an output parameter or input/output parameters, you must call `FlushResultSet` until it returns `FALSE` (the value 0), in order to obtain these parameter values.  
  
 `FlushResultSet` calls the ODBC API function `SQLMoreResults`. If `SQLMoreResults` returns `SQL_ERROR` or `SQL_INVALID_HANDLE`, then `FlushResultSet` will throw an exception. For more information about `SQLMoreResults`, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 Your stored procedure needs to have bound fields if you want to call `FlushResultSet`.  
  
## Exceptions  
 This method can throw exceptions of type `CDBException*`.  
  
## Example  
 The following code assumes that `COutParamRecordset` is a `CRecordset`-derived object based on a predefined query with an input parameter and an output parameter, and having multiple result sets. Note the structure of the [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md) override.  
  
 [!CODE [NVC_MFCDatabase#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#21)]  
  
 [!CODE [NVC_MFCDatabase#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#22)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFieldExchange::SetFieldType](../vs140/CFieldExchange--SetFieldType.md)