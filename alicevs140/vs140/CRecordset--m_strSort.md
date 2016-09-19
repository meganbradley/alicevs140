---
title: "CRecordset::m_strSort"
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
ms.assetid: 34dc533c-a670-4208-91a9-b63b38944d9c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::m_strSort
After you construct the recordset object, but before you call its **Open** member function, use this data member to store a `CString` containing a SQL **ORDER BY** clause.  
  
## Remarks  
 The recordset uses this string to sort the records it selects during the **Open** or **Requery** call. You can use this feature to sort a recordset on one or more columns. The ODBC SQL syntax for an **ORDER BY** clause is  
  
 `ORDER BY sort-specification [, sort-specification]...`  
  
 where a sort-specification is an integer or a column name. You can also specify ascending or descending order (the order is ascending by default) by appending "ASC" or "DESC" to the column list in the sort string. The selected records are sorted first by the first column listed, then by the second, and so on. For example, you might order a "Customers" recordset by last name, then first name. The number of columns you can list depends on the data source. For more information, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 Note that you do not include the **ORDER BY** keyword in your string. The framework supplies it.  
  
 For more information about SQL clauses, see the article [SQL](../vs140/SQL.md). For more information about sorting records, see the article [Recordset: Sorting Records (ODBC)](../vs140/Recordset--Sorting-Records--ODBC-.md).  
  
## Example  
 [!CODE [NVC_MFCDatabase#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#31)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::m_strFilter](../vs140/CRecordset--m_strFilter.md)   
 [CRecordset::Requery](../vs140/CRecordset--Requery.md)