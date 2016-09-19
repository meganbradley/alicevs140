---
title: "CDatabase::ExecuteSQL"
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
ms.assetid: f019e896-136b-4e35-bb78-08f87dac2054
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::ExecuteSQL
Call this member function when you need to execute a SQL command directly.  
  
## Syntax  
  
```  
  
      void ExecuteSQL(   
   LPCTSTR lpszSQL    
);  
```  
  
#### Parameters  
 `lpszSQL`  
 Pointer to a null-terminated string containing a valid SQL command to execute. You can pass a [CString](../vs140/CStringT-Class.md).  
  
## Remarks  
 Create the command as a null-terminated string. `ExecuteSQL` does not return data records. If you want to operate on records, use a recordset object instead.  
  
 Most of your commands for a data source are issued through recordset objects, which support commands for selecting data, inserting new records, deleting records, and editing records. However, not all ODBC functionality is directly supported by the database classes, so you may at times need to make a direct SQL call with `ExecuteSQL`.  
  
## Example  
 [!CODE [NVC_MFCDatabase#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#13)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::SetLoginTimeout](../vs140/CDatabase--SetLoginTimeout.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)