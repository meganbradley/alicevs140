---
title: "CRecordset::GetDefaultConnect"
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
ms.assetid: 67499451-fe0e-4324-92a9-70e3d813be10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetDefaultConnect
Called to get the default connection string.  
  
## Syntax  
  
```  
  
virtual CString GetDefaultConnect( );  
```  
  
## Return Value  
 A `CString` that contains the default connection string.  
  
## Remarks  
 The framework calls this member function to get the default connection string for the data source on which the recordset is based. ClassWizard implements this function for you by identifying the same data source you use in ClassWizard to get information about tables and columns. You will probably find it convenient to rely on this default connection while developing your application. But the default connection may not be appropriate for users of your application. If that is the case, you should reimplement this function, discarding ClassWizard's version. For more information about connection strings, see the article [Data Source (ODBC)](../vs140/Data-Source--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)