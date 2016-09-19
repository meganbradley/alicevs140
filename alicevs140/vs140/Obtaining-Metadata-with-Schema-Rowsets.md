---
title: "Obtaining Metadata with Schema Rowsets"
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
ms.assetid: 6b448461-82fb-4acf-816b-3cbb0ca1d186
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Obtaining Metadata with Schema Rowsets
Sometimes you need to obtain information about the provider, rowset, table, columns, or other database information without opening the rowset. Data about the database structure is called metadata and can be retrieved by a number of different methods. One method is to use schema rowsets.  
  
 OLE DB Templates provide a set of classes to retrieve schema information; these classes create predefined schema rowsets and are listed in [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md).  
  
> [!NOTE]
>  If you are using OLAP and some of your rowsets are not supported by the schema rowset classes (for example, you have a variable number of columns), you should consider using `CManualAccessor` or `CDynamicAccessor`. You can scroll through the columns and use case statements to handle the possible data types for each column.  
  
## Catalog/Schema Model  
 ANSI SQL defines a catalog/schema model for data stores; OLE DB uses this model. In this model, catalogs (databases) contain schemas and schemas contain tables.  
  
-   **Catalog** A catalog is another name for a database. It is a collection of related schemas. To list the catalogs (databases) belonging to a given data source, use [CCatalog](../vs140/CCatalogs--CCatalogInfo.md). Because many databases have only one catalog, metadata is sometimes simply called schema information.  
  
-   **Schema** A schema is a collection of database objects that are owned or have been created by a particular user. To list the schemas owned by a given user, use [CSchemata](../vs140/CSchemata--CSchemataInfo.md).  
  
     In Microsoft SQL Server and ODBC 2.x terms, a schema is an owner (for example, dbo is a typical schema name). Also, SQL Server stores metadata in a set of tables: one table contains a list of all the tables and another table contains a list of all the columns. There is no equivalent to a schema in a Microsoft Access database.  
  
-   **Table** Tables are collections of columns arranged in specific orders. To list the tables defined in a given catalog (database) and information about those tables, use [CTables](../vs140/CTables--CTableInfo.md)).  
  
## Restrictions  
 When you query for schema information, you can use restrictions to specify the type of information in which you are interested. You can think of restrictions as a filter or qualifier in a query. For example, in the query:  
  
```  
SELECT * FROM authors where l_name = 'pivo'  
```  
  
 `l_name` is a restriction. This is a very simple example with only one restriction; the schema rowset classes support several restrictions.  
  
 The [schema rowset typedef classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md) encapsulate all the OLE DB schema rowsets so that you can access a schema rowset just like any other rowset by instantiating and opening it. For example, the typedef class [CColumns](../vs140/CColumns--CColumnsInfo.md) is defined as:  
  
```  
CRestrictions<CAccessor<CColumnsInfo>  
```  
  
 The [CRestrictions](../vs140/CRestrictions-Class.md) class supplies the restriction support. After you create an instance of the schema rowset, call [CRestrictions::Open](../vs140/CRestrictions--Open.md). This method returns a result set based on the restrictions that you specify.  
  
 To specify restrictions, refer to [Appendix B: Schema Rowsets](http://go.microsoft.com/fwlink/?LinkId=64681) and look up the rowset that you are using. For example, **CColumns** corresponds to the [COLUMNS Rowset](http://go.microsoft.com/fwlink/?LinkId=64682); that topic lists the restriction columns in the COLUMNS rowset: TABLE_CATALOG, TABLE_SCHEMA, TABLE_NAME, COLUMN_NAME. You must follow that order in specifying your restrictions.  
  
 So, for example, if you want to restrict by table name, note that TABLE_NAME is the third restriction column, and then call **Open**, specifying the desired table name as the third restriction parameter, as shown in the following example.  
  
#### To use schema rowsets  
  
1.  You must include the header file Atldbsch.h (of course, you need Atldbcli.h for consumer support as well).  
  
2.  Instantiate a schema rowset object in the consumer's or the document's header file. If you want table information, declare a **CTables** object; if you want column information, declare a **CColumns** object. This example shows how to retrieve the columns in the authors table:  
  
    ```  
    CDataSource ds;  
    ds.Open();  
    CSession ss;  
    ss.Open();  
    CColumns ColumnSchemaRowset;  
    // TABLE_NAME is the third restriction column, so  
    // specify "authors" as the third restriction parameter:  
    hr = ColumnSchemaRowset.Open(ss, NULL, NULL, "authors");  
    hr = ColumnSchemaRowset.MoveFirst();  
    while (hr == S_OK)  
    {  
       hr = ColumnSchemaRowset.MoveNext();  
    }  
    ```  
  
3.  To fetch the information, access the appropriate data member of the schema rowset object, for example, `ColumnSchemaRowset.m_szColumnName`. This corresponds to COLUMN_NAME. To see which OLE DB column each data member corresponds to, see [CColumns](../vs140/CColumns--CColumnsInfo.md).  
  
 For the reference of the schema rowset, typedef classes provided in the OLE DB Templates (see [Schema Rowset Classes and Typedef Classes](../vs140/Schema-Rowset-Classes-and-Typedef-Classes.md)).  
  
 For more information about OLE DB schema rowsets, including restriction columns, see [Appendix B: Schema Rowsets](http://go.microsoft.com/fwlink/?LinkId=64681) in the OLE DB Programmer's Reference.  
  
 For more complex examples of how to use schema rowset classes, see the [CatDB](assetId:///003d516b-2bf6-444e-8be5-4ebaa0b66046) and [DBViewer](assetId:///07620f99-c347-4d09-9ebc-2459e8049832) samples.  
  
 For information about provider support for schema rowsets, see [Supporting Schema Rowsets](../vs140/Supporting-Schema-Rowsets.md).  
  
## See Also  
 [Using Accessors](../vs140/Using-Accessors.md)