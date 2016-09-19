---
title: "Catalog Information  (MFC Data Access)"
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
ms.assetid: c184e80f-ff17-409f-9df8-05275080bb8d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Catalog Information  (MFC Data Access)
Information about the tables in a data source can include the names of tables and the columns in them, table privileges, names of primary and foreign keys, information about predefined queries or stored procedures, information about indexes on tables, and statistics about tables.  
  
 For more information, see [Data Source: Determining the Schema of the Data Source (ODBC)](../vs140/Data-Source--Determining-the-Schema-of-the-Data-Source--ODBC-.md).  
  
> [!NOTE]
>  In the MFC DAO classes, you can get catalog information as follows: Use [CDaoDatabase::GetTableDefCount](../vs140/CDaoDatabase--GetTableDefCount.md) and [CDaoDatabase::GetTableDefInfo](../vs140/CDaoDatabase--GetTableDefInfo.md) to enumerate the tables in the database and obtain information for each table in a [CDaoTableDefInfo](../vs140/CDaoTableDefInfo-Structure.md) structure.  
  
## See Also  
 [Data Access Programming (MFC/ATL)](../vs140/Data-Access-Programming--MFC-ATL-.md)