---
title: "CRecordset::GetSQL"
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
ms.assetid: f6d23a71-872f-474c-8d06-1c1f43f4febb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetSQL
Call this member function to get the SQL statement that was used to select the recordset's records when it was opened.  
  
## Syntax  
  
```  
  
const CString& GetSQL( ) const;  
```  
  
## Return Value  
 A **const** reference to a `CString` that contains the SQL statement.  
  
## Remarks  
 This will generally be a SQL **SELECT** statement. The string returned by `GetSQL` is read-only.  
  
 The string returned by `GetSQL` is typically different from any string you may have passed to the recordset in the `lpszSQL` parameter to the **Open** member function. This is because the recordset constructs a full SQL statement based on what you passed to **Open**, what you specified with ClassWizard, what you may have specified in the **m_strFilter** and `m_strSort` data members, and any parameters you may have specified. For details about how the recordset constructs this SQL statement, see the article [Recordset: How Recordsets Select Records (ODBC)](../vs140/Recordset--How-Recordsets-Select-Records--ODBC-.md).  
  
> [!NOTE]
>  Call this member function only after calling [Open](../vs140/CRecordset--Open.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::GetDefaultSQL](../vs140/CRecordset--GetDefaultSQL.md)   
 [CRecordset::Open](../vs140/CRecordset--Open.md)   
 [CRecordset::m_strFilter](../vs140/CRecordset--m_strFilter.md)   
 [CRecordset::m_strSort](../vs140/CRecordset--m_strSort.md)