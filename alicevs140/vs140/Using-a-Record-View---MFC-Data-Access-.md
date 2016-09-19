---
title: "Using a Record View  (MFC Data Access)"
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
ms.topic: article
ms.assetid: 91f2828f-0666-4273-ae28-e4703fd98521
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using a Record View  (MFC Data Access)
This topic explains how you might commonly customize the default code for record views that the wizard writes for you. Typically, you want to constrain the record selection with a [filter](../vs140/Recordset--Filtering-Records--ODBC-.md) or [parameters](../vs140/Recordset--Parameterizing-a-Recordset--ODBC-.md), perhaps [sort](../vs140/Recordset--Sorting-Records--ODBC-.md) the records, customize the SQL statement.  
  
 This information applies to both [CRecordView](../vs140/CRecordView-Class.md) (ODBC) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) (DAO).  
  
 Using `CRecordView` or `CDaoRecordView` is much the same as using [CFormView](../vs140/CFormView-Class.md). The basic approach is to use the record view to display and perhaps update the records of a single recordset. Beyond that, you might want to use other recordsets as well, as discussed in [Record Views: Filling a List Box from a Second Recordset](../vs140/Filling-a-List-Box-from-a-Second-Recordset---MFC-Data-Access-.md).  
  
## See Also  
 [Record Views  (MFC Data Access)](../vs140/Record-Views---MFC-Data-Access-.md)   
 [ODBC Driver List](../vs140/ODBC-Driver-List.md)