---
title: "ODBC Classes"
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
ms.assetid: 6c40fca8-3033-4873-9abe-7f51725de0e0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ODBC Classes
These classes work with the other application framework classes to give easy access to a wide variety of databases for which Open Database Connectivity (ODBC) drivers are available.  
  
 Programs that use ODBC databases will have at least a `CDatabase` object and a `CRecordset` object.  
  
 [CDatabase](../vs140/CDatabase-Class.md)  
 Encapsulates a connection to a data source, through which you can operate on the data source.  
  
 [CRecordset](../vs140/CRecordset-Class.md)  
 Encapsulates a set of records selected from a data source. Recordsets enable scrolling from record to record, updating records (adding, editing, and deleting records), qualifying the selection with a filter, sorting the selection, and parameterizing the selection with information obtained or calculated at run time.  
  
 [CRecordView](../vs140/CRecordView-Class.md)  
 Provides a form view directly connected to a recordset object. The dialog data exchange (DDX) mechanism exchanges data between the recordset and the controls of the record view. Like all form views, a record view is based on a dialog template resource. Record views also support moving from record to record in the recordset, updating records, and closing the associated recordset when the record view closes.  
  
 [CDBException](../vs140/CDBException-Class.md)  
 An exception resulting from failures in data access processing. This class serves the same purpose as other exception classes in the exception-handling mechanism of the class library.  
  
 [CFieldExchange](../vs140/CFieldExchange-Class.md)  
 Supplies context information to support record field exchange (RFX), which exchanges data between the field data members and parameter data members of a recordset object and the corresponding table columns on the data source. Analogous to class [CDataExchange](../vs140/CDataExchange-Class.md), which is used similarly for dialog data exchange (DDX).  
  
## Related Classes  
 [CLongBinary](../vs140/CLongBinary-Class.md)  
 Encapsulates a handle to storage for a binary large object (BLOB), such as a bitmap. `CLongBinary` objects are used to manage large data objects stored in database tables.  
  
 [CDBVariant](../vs140/CDBVariant-Class.md)  
 Allows you to store a value without worrying about the value's data type. `CDBVariant` tracks the data type of the current value, which is stored in a union.  
  
## See Also  
 [Class Overview](../vs140/Class-Library-Overview.md)