---
title: "Record Field Exchange (RFX)"
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
ms.assetid: f5ddfbf0-2901-48d7-9848-4fb84de3c7ee
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Record Field Exchange (RFX)
The MFC ODBC database classes automate moving data between the data source and a [recordset](../vs140/Recordset--ODBC-.md) object. When you derive a class from [CRecordset](../vs140/CRecordset-Class.md) and do not use bulk row fetching, data is transferred by the record field exchange (RFX) mechanism.  
  
> [!NOTE]
>  If you have implemented bulk row fetching in a derived `CRecordset` class, the framework uses the bulk record field exchange (Bulk RFX) mechanism to transfer data. For more information, see [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 RFX is similar to dialog data exchange (DDX). Moving data between a data source and the field data members of a recordset requires multiple calls to the recordset's [DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md) function and considerable interaction between the framework and [ODBC](../vs140/ODBC-Basics.md). The RFX mechanism is type-safe and saves you the work of calling ODBC functions such as **::SQLBindCol**. For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
 RFX is mostly transparent to you. If you declare your recordset classes with the MFC Application Wizard or **Add Class** (as described in [Adding an MFC ODBC Consumer](../vs140/Adding-an-MFC-ODBC-Consumer.md)), RFX is built into them automatically. Your recordset class must be derived from the base class `CRecordset` supplied by the framework. The MFC Application Wizard lets you create an initial recordset class. **Add Class** lets you add other recordset classes as you need them. For more information and examples, see [Adding an MFC ODBC Consumer](../vs140/Adding-an-MFC-ODBC-Consumer.md).  
  
 You must manually add a small amount of RFX code in three cases, when you want to:  
  
-   Use parameterized queries. For more information, see [Recordset: Parameterizing a Recordset (ODBC)](../vs140/Recordset--Parameterizing-a-Recordset--ODBC-.md).  
  
-   Perform joins (using one recordset for columns from two or more tables). For more information, see [Recordset: Performing a Join (ODBC)](../vs140/Recordset--Performing-a-Join--ODBC-.md).  
  
-   Bind data columns dynamically. This is less common than parameterization. For more information, see [Recordset: Dynamically Binding Data Columns (ODBC)](../vs140/Recordset--Dynamically-Binding-Data-Columns--ODBC-.md).  
  
 If you need a more advanced understanding of RFX, see [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md).  
  
 The following topics explain the details of using recordset objects:  
  
-   [Record Field Exchange: Using RFX](../vs140/Record-Field-Exchange--Using-RFX.md)  
  
-   [Record Field Exchange: Using the RFX Functions](../vs140/Record-Field-Exchange--Using-the-RFX-Functions.md)  
  
-   [Record Field Exchange: How RFX Works](../vs140/Record-Field-Exchange--How-RFX-Works.md)  
  
## See Also  
 [Open Database Connectivity (ODBC)](../vs140/Open-Database-Connectivity--ODBC-.md)   
 [Recordset (ODBC)](../vs140/Recordset--ODBC-.md)   
 [MFC ODBC Consume](../vs140/Adding-an-MFC-ODBC-Consumer.md)   
 [Database Support, MFC Application Wizard](../vs140/Database-Support--MFC-Application-Wizard.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)