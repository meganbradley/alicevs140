---
title: "CDaoRecordset::GetDefaultDBName"
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
ms.assetid: 366a1b18-a0c6-459a-9944-d060c86aa4c8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetDefaultDBName
Call this member function to determine the name of the database for this recordset.  
  
## Syntax  
  
```  
  
virtual CString GetDefaultDBName( );  
  
```  
  
## Return Value  
 A `CString` that contains the path and name of the database from which this recordset is derived.  
  
## Remarks  
 If a recordset is created without a pointer to a [CDaoDatabase](../vs140/CDaoDatabase-Class.md), then this path is used by the recordset to open the default database. By default, this function returns an empty string. When ClassWizard derives a new recordset from `CDaoRecordset`, it will create this function for you.  
  
 The following example illustrates the use of the double backslash (\\\\) in the string, as is required for the string to be interpreted correctly.  
  
 [!CODE [NVC_MFCDatabase#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#4)]  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetDefaultSQL](../vs140/CDaoRecordset--GetDefaultSQL.md)   
 [CDaoRecordset::GetName](../vs140/CDaoRecordset--GetName.md)   
 [CDaoRecordset::GetSQL](../vs140/CDaoRecordset--GetSQL.md)   
 [CDaoRecordset::GetType](../vs140/CDaoRecordset--GetType.md)