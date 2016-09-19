---
title: "CRecordset::OnSetOptions"
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
ms.assetid: 9b8add17-44e7-41f8-86ce-88b5e0282329
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::OnSetOptions
Called to set options (used on selection) for the specified ODBC statement.  
  
## Syntax  
  
```  
  
      virtual void OnSetOptions(  
   HSTMT hstmt   
);  
```  
  
#### Parameters  
 `hstmt`  
 The **HSTMT** of the ODBC statement whose options are to be set.  
  
## Remarks  
 Call `OnSetOptions` to set options (used on selection) for the specified ODBC statement. The framework calls this member function to set initial options for the recordset. `OnSetOptions` determines the data source's support for scrollable cursors and for cursor concurrency and sets the recordset's options accordingly. (Whereas `OnSetOptions` is used for selection operations, `OnSetUpdateOptions` is used for update operations.)  
  
 Override `OnSetOptions` to set options specific to the driver or the data source. For example, if your data source supports opening for exclusive access, you might override `OnSetOptions` to take advantage of that ability.  
  
 For more information about cursors, see the article [ODBC](../vs140/ODBC-Basics.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::OnSetOptions](../vs140/CDatabase--OnSetOptions.md)   
 [CRecordset::OnSetUpdateOptions](../vs140/CRecordset--OnSetUpdateOptions.md)