---
title: "CRecordset::OnSetUpdateOptions"
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
ms.assetid: d60523f0-20df-418b-a196-c37bb7849c03
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::OnSetUpdateOptions
Called to set options (used on update) for the specified ODBC statement.  
  
## Syntax  
  
```  
  
      virtual void OnSetUpdateOptions(  
   HSTMT hstmt   
);  
```  
  
#### Parameters  
 `hstmt`  
 The **HSTMT** of the ODBC statement whose options are to be set.  
  
## Remarks  
 Call `OnSetUpdateOptions` to set options (used on update) for the specified ODBC statement. The framework calls this member function after it creates an HSTMT to update records in a recordset. (Whereas `OnSetOptions` is used for selection operations, `OnSetUpdateOptions` is used for update operations.) `OnSetUpdateOptions` determines the data source's support for scrollable cursors and for cursor concurrency and sets the recordset's options accordingly.  
  
 Override `OnSetUpdateOptions` to set options of an ODBC statement before that statement is used to access a database.  
  
 For more information about cursors, see the article [ODBC](../vs140/ODBC-Basics.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OnSetOptions](../vs140/CDatabase--OnSetOptions.md)   
 [CRecordset::OnSetOptions](../vs140/CRecordset--OnSetOptions.md)