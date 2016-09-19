---
title: "Recordset: Working with Large Data Items (ODBC)"
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
ms.assetid: 3e80b5a8-b6e7-43c6-a816-e54befc513a3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recordset: Working with Large Data Items (ODBC)
This topic applies to both the MFC ODBC classes and the MFC DAO classes.  
  
> [!NOTE]
>  If you are using the MFC DAO classes, manage your large data items with class [CByteArray](../vs140/CByteArray-Class.md) rather than class [CLongBinary](../vs140/CLongBinary-Class.md). If you are using the MFC ODBC classes with bulk row fetching, use `CLongBinary` rather than `CByteArray`. For more information about bulk row fetching, see [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 Suppose your database can store large pieces of data, such as bitmaps (employee photographs, maps, pictures of products, OLE objects, and so on). This kind of data is often referred to as a Binary Large Object (or BLOB) because:  
  
-   Each field value is large.  
  
-   Unlike numbers and other simple data types, it has no predictable size.  
  
-   The data is formless from the perspective of your program.  
  
 This topic explains what support the database classes provide for working with such objects.  
  
##  <a name="_core_managing_large_objects"></a> Managing Large Objects  
 Recordsets have two ways to solve the special difficulty of managing binary large objects. You can use class [CByteArray](../vs140/CByteArray-Class.md) or you can use class [CLongBinary](../vs140/CLongBinary-Class.md). In general, `CByteArray` is the preferred way to manage large binary data.  
  
 `CByteArray` requires more overhead than `CLongBinary` but is more capable, as described in [The CByteArray Class](#_core_the_cbytearray_class). `CLongBinary` is described briefly in [The CLongBinary Class](#_core_the_clongbinary_class).  
  
 For detailed information about using `CByteArray` to work with large data items, see [Technical Note 45](../vs140/TN045--MFC-Database-Support-for-Long-Varchar-Varbinary.md).  
  
##  <a name="_core_the_cbytearray_class"></a> CByteArray Class  
 `CByteArray` is one of the MFC collection classes. A `CByteArray` object stores a dynamic array of bytes — the array can grow if needed. The class provides fast access by index, as with built-in C++ arrays. `CByteArray` objects can be serialized and dumped for diagnostic purposes. The class supplies member functions for getting and setting specified bytes, inserting and appending bytes, and removing one byte or all bytes. These facilities make parsing the binary data easier. For example, if the binary object is an OLE object, you might have to work through some header bytes to reach the actual object.  
  
##  <a name="_core_using_cbytearray_in_recordsets"></a> Using CByteArray in Recordsets  
 By giving a field data member of your recordset the type `CByteArray`, you provide a fixed base from which [RFX](../vs140/Record-Field-Exchange--RFX-.md) can manage the transfer of such an object between your recordset and the data source and through which you can manipulate the data inside the object. RFX needs a specific site for retrieved data, and you need a way to access the underlying data.  
  
 For detailed information about using `CByteArray` to work with large data items, see [Technical Note 45](../vs140/TN045--MFC-Database-Support-for-Long-Varchar-Varbinary.md).  
  
##  <a name="_core_the_clongbinary_class"></a> CLongBinary Class  
 A [CLongBinary](../vs140/CLongBinary-Class.md) object is a simple shell around an `HGLOBAL` handle to a block of storage allocated on the heap. When it binds a table column containing a binary large object, RFX allocates the `HGLOBAL` handle when it needs to transfer the data to the recordset and stores the handle in the `CLongBinary` field of the recordset.  
  
 In turn, you use the `HGLOBAL` handle, `m_hData`, to work with the data itself, operating on it as you would on any handle data. This is where [CByteArray](../vs140/CByteArray-Class.md) adds capabilities.  
  
> [!CAUTION]
>  CLongBinary objects cannot be used as parameters in function calls. In addition, their implementation, which calls **::SQLGetData**, necessarily slows scrolling performance for a scrollable snapshot. This might also be true when you use an **::SQLGetData** call yourself to retrieve dynamic schema columns.  
  
## See Also  
 [Recordset (ODBC)](../vs140/Recordset--ODBC-.md)   
 [Recordset: Obtaining SUMs and Other Aggregate Results (ODBC)](../vs140/Recordset--Obtaining-SUMs-and-Other-Aggregate-Results--ODBC-.md)   
 [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md)