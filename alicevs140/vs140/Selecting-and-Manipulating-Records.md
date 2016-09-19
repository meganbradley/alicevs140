---
title: "Selecting and Manipulating Records"
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
ms.assetid: 7f0b3a4a-9941-4475-a612-9ec8d15b7691
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Selecting and Manipulating Records
Normally when you select records from a data source using a SQL **SELECT** statement, you get a result set, which is a set of records from a table or a query. With the database classes, you use a recordset object to select and access the result set. This is an object of an application-specific class that you derive from class [CRecordset](../vs140/CRecordset-Class.md). When you define a recordset class, you specify the data source to associate it with, the table to use, and the columns of the table. The MFC Application Wizard or **Add Class** (as described in [Adding an MFC ODBC Consumer](../vs140/Adding-an-MFC-ODBC-Consumer.md)) creates a class with a connection to a specific data source. The wizards write the [GetDefaultSQL](../vs140/CRecordset--GetDefaultSQL.md) member function of class `CRecordset` to return the table name. For more information about using the wizards to create recordset classes, see [Database Support, MFC Application Wizard](../vs140/Database-Support--MFC-Application-Wizard.md) and [Adding an MFC ODBC Consumer](../vs140/Adding-an-MFC-ODBC-Consumer.md).  
  
 Using a [CRecordset](../vs140/CRecordset-Class.md) object at run time, you can:  
  
-   Examine the data fields of the current record.  
  
-   Filter or sort the recordset.  
  
-   Customize the default SQL **SELECT** statement.  
  
-   Scroll through the selected records.  
  
-   Add, update, or delete records (if both the data source and the recordset are updateable).  
  
-   Test whether the recordset allows requerying and refresh the recordset's contents.  
  
 When you finish using the recordset object, you close and destroy it. For more information about recordsets, see [Recordset (ODBC)](../vs140/Recordset--ODBC-.md).  
  
## See Also  
 [ODBC and MFC](../vs140/ODBC-and-MFC.md)