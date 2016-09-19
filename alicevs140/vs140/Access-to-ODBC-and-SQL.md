---
title: "Access to ODBC and SQL"
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
ms.assetid: 5613d7dc-00b7-4646-99ae-1116c05c52b4
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Access to ODBC and SQL
The Microsoft Foundation Class Library encapsulates many Windows API calls and still lets you call any Windows API function directly. The database classes give you the same flexibility with regard to the ODBC API. While the database classes shield you from much of the complexity of ODBC, you can call ODBC API functions directly from anywhere in your program.  
  
 Similarly, the database classes shield you from having to work much with [SQL](../vs140/SQL.md), but you can use SQL directly if you want. You can customize recordset objects by passing a custom SQL statement (or setting portions of the default statement) when you open the recordset. You can also make SQL calls directly using the [ExecuteSQL](../vs140/CDatabase--ExecuteSQL.md) member function of class [CDatabase](../vs140/CDatabase-Class.md).  
  
 For more information, see [ODBC: Calling ODBC API Functions Directly](../vs140/ODBC--Calling-ODBC-API-Functions-Directly.md) and [SQL: Making Direct SQL Calls (ODBC)](../vs140/SQL--Making-Direct-SQL-Calls--ODBC-.md).  
  
## See Also  
 [ODBC and MFC](../vs140/ODBC-and-MFC.md)