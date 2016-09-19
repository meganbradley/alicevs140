---
title: "SQL"
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
ms.assetid: e3923bc4-b317-4e0b-afd8-3cd403eb0faf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SQL
SQL (Structured Query Language) is a way to communicate with a relational database that lets you define, query, modify, and control the data. Using SQL syntax, you can construct a statement that extracts records according to criteria you specify.  
  
> [!NOTE]
>  This information applies to the MFC ODBC classes. If you are working with the MFC DAO classes, see the topic Comparison of Microsoft Jet Database Engine SQL and ANSI SQL in DAO Help.  
  
 SQL statements begin with a keyword verb such as **CREATE** or **SELECT**. SQL is a very powerful language; a single statement can affect an entire table.  
  
 Many versions of SQL exist, each developed with a particular DBMS in mind. The MFC database classes recognize a set of SQL statements that corresponds to the X/Open and SQL Access Group Common Applications Environment (CAE) SQL draft specification (1991). For information about the syntax of these statements, see Appendix C in the *ODBC SDK* *Programmer's Reference* on the MSDN Library CD.  
  
 This topic explains:  
  
-   [The relationship between ODBC and SQL](#_core_open_database_connectivity_.28.odbc.29).  
  
-   [The most common SQL keywords used by the database classes](#_core_the_database_classes).  
  
-   [How the database classes use SQL](#_core_how_the_database_classes_use_sql).  
  
##  <a name="_core_open_database_connectivity_.28.odbc.29"></a> Open Database Connectivity (ODBC)  
 The database classes are implemented with ODBC, which uses SQL in a call-level interface rather than embedding SQL commands in the code. ODBC uses SQL to communicate with a [data source](../vs140/Data-Source--ODBC-.md) through ODBC drivers. These drivers interpret the SQL and translate it, if necessary, for use with a particular database format, such as Microsoft Access. For more information about how ODBC uses SQL, see [ODBC](../vs140/ODBC-Basics.md) and the ODBC SDK *Programmer's Reference* on the MSDN Library CD.  
  
##  <a name="_core_the_database_classes"></a> Database Classes  
 The database classes are designed to let you manipulate and update data in an existing [data source](../vs140/Data-Source--ODBC-.md). The [MFC Application Wizard](../vs140/Database-Support--MFC-Application-Wizard.md), the [MFC ODBC Consumer Wizard](../vs140/Adding-an-MFC-ODBC-Consumer.md) (accessed through **Add Class**), and the database classes construct most of the SQL statements for you.  
  
 The database classes use a portion of SQL known as the Data Manipulation Language (DML). These commands let you work with all or part of the data source, add new records, edit records, and delete records. The following table lists the most common SQL keywords and the ways the database classes use them.  
  
### Some Common SQL Keywords  
  
|SQL keyword|The wizards and database classes use it|  
|-----------------|---------------------------------------------|  
|**SELECT**|To identify which tables and columns in the data source are to be used.|  
|**WHERE**|To apply a filter that narrows the selection.|  
|**ORDER BY**|To apply a sort order to the recordset.|  
|**INSERT**|To add new records to a recordset.|  
|**DELETE**|To delete records from a recordset.|  
|**UPDATE**|To modify the fields of a record.|  
  
 In addition, the database classes recognize ODBC **CALL** statements, which you can use to call a predefined query (or stored procedure) on some data sources. The ODBC database driver interprets these statements and substitutes the command appropriate for each DBMS.  
  
> [!NOTE]
>  Not all DBMSs support **CALL** statements.  
  
 If the classes cannot recognize a user-supplied statement in `CRecordset::Open`, it is interpreted as a table name.  
  
 For an explanation of how the framework constructs SQL statements, see [Recordset: How Recordsets Select Records (ODBC)](../vs140/Recordset--How-Recordsets-Select-Records--ODBC-.md) and [SQL: Customizing Your Recordset's SQL Statement (ODBC)](../vs140/SQL--Customizing-Your-Recordset’s-SQL-Statement--ODBC-.md).  
  
 SQL databases use data types similar to those used in C and C++. For a discussion of these similarities, see [SQL: SQL and C++ Data Types (ODBC)](../vs140/SQL--SQL-and-C---Data-Types--ODBC-.md).  
  
 You can find more information about SQL, including a list of supported SQL statements, data types, SQL core grammar, and a reading list of recommended publications about SQL, in the *ODBC SDK* *Programmer's Reference* on the MSDN Library CD.  
  
##  <a name="_core_how_the_database_classes_use_sql"></a> How the Database Classes Use SQL  
 The recordsets you derive from the database classes use ODBC to communicate with a data source, and ODBC retrieves records from the data source by sending SQL statements. This topic explains the relationship between the database classes and SQL.  
  
 A recordset constructs a SQL statement by building up the pieces of a SQL statement into a `CString`. The string is constructed as a **SELECT** statement, which returns a set of records.  
  
 When the recordset calls ODBC to send a SQL statement to the data source, the ODBC Driver Manager passes the statement to the ODBC driver and the driver sends it to the underlying DBMS. The DBMS returns a result set of records, and the ODBC driver returns the records to the application. The database classes let your program access the result set in a type-safe C++ class derived from `CRecordset`.  
  
 The following topics provide more information about how the database classes use SQL:  
  
-   [SQL: Customizing Your Recordset's SQL Statement (ODBC)](../vs140/SQL--Customizing-Your-Recordset’s-SQL-Statement--ODBC-.md)  
  
-   [SQL: SQL and C++ Data Types (ODBC)](../vs140/SQL--SQL-and-C---Data-Types--ODBC-.md)  
  
-   [SQL: Making Direct SQL Calls (ODBC)](../vs140/SQL--Making-Direct-SQL-Calls--ODBC-.md)  
  
## See Also  
 [Open Database Connectivity (ODBC)](../vs140/Open-Database-Connectivity--ODBC-.md)   
 [ODBC Basics](../vs140/ODBC-Basics.md)