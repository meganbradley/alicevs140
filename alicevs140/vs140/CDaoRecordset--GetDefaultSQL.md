---
title: "CDaoRecordset::GetDefaultSQL"
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
ms.assetid: 0d59f7fe-9e6a-4a3b-a7ad-0ec765ba0740
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetDefaultSQL
The framework calls this member function to get the default SQL statement on which the recordset is based.  
  
## Syntax  
  
```  
  
virtual CString GetDefaultSQL( );  
  
```  
  
## Return Value  
 A `CString` that contains the default SQL statement.  
  
## Remarks  
 This might be a table name or a SQL **SELECT** statement.  
  
 You indirectly define the default SQL statement by declaring your recordset class with ClassWizard, and ClassWizard performs this task for you.  
  
 If you pass a null SQL string to [Open](../vs140/CDaoRecordset--Open.md), then this function is called to determine the table name or SQL for your recordset.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetDefaultDBName](../vs140/CDaoRecordset--GetDefaultDBName.md)   
 [CDaoRecordset::GetName](../vs140/CDaoRecordset--GetName.md)   
 [CDaoRecordset::GetSQL](../vs140/CDaoRecordset--GetSQL.md)   
 [CDaoRecordset::GetType](../vs140/CDaoRecordset--GetType.md)