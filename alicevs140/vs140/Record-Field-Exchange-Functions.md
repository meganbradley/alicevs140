---
title: "Record Field Exchange Functions"
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
ms.assetid: 6e4c5c1c-acb7-4c18-bf51-bf7959a696cd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Record Field Exchange Functions
This topic lists the Record Field Exchange ([RFX](#_mfc_rfx_functions_.28.odbc.29), [Bulk RFX](#_mfc_bulk_rfx_functions_.28.odbc.29), and [DFX](#_mfc_dfx_functions_.28.dao.29)) functions used to automate the transfer of data between a recordset object and its data source and to perform other operations on the data.  
  
 If you are using the ODBC-based classes and you have implemented bulk row fetching, you must manually override the `DoBulkFieldExchange` member function of `CRecordset` by calling the Bulk RFX functions for each data member corresponding to a data source column.  
  
 If you have not implemented bulk row fetching in the ODBC-based classes, or if you are using the DAO-based classes, then ClassWizard will override the `DoFieldExchange` member function of `CRecordset` or `CDaoRecordset` by calling the RFX functions (for ODBC classes) or the DFX functions (for DAO classes) for each field data member in your recordset.  
  
 The record field exchange functions transfer data each time the framework calls `DoFieldExchange` or `DoBulkFieldExchange`. Each function transfers a specific data type.  
  
 For more information about how these functions are used, see the articles [Record Field Exchange: How RFX Works (ODBC)](../vs140/Record-Field-Exchange--How-RFX-Works.md). For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 For columns of data that you bind dynamically, you can also call the RFX or DFX functions yourself, as explained in the articles [Recordset: Dynamically Binding Data Columns (ODBC)](../vs140/Recordset--Dynamically-Binding-Data-Columns--ODBC-.md). Additionally, you can write your own custom RFX or DFX routines, as explained in Technical Note [43](../vs140/TN043--RFX-Routines.md) (for ODBC) and Technical Note [53](../vs140/TN053--Custom-DFX-Routines-for-DAO-Database-Classes.md) (for DAO).  
  
 For an example of RFX and Bulk RFX functions as they appear in the `DoFieldExchange` and `DoBulkFieldExchange` functions, see [RFX_Text](../vs140/RFX_Text.md) and [RFX_Text_Bulk](../vs140/RFX_Text_Bulk.md). DFX functions are very similar to the RFX functions.  
  
### RFX Functions (ODBC)  
  
|||  
|-|-|  
|[RFX_Binary](../vs140/RFX_Binary.md)|Transfers arrays of bytes of type [CByteArray](../vs140/CByteArray-Class.md).|  
|[RFX_Bool](../vs140/RFX_Bool.md)|Transfers Boolean data.|  
|[RFX_Byte](../vs140/RFX_Byte.md)|Transfers a single byte of data.|  
|[RFX_Date](../vs140/RFX_Date.md)|Transfers time and date data using [CTime](../Topic/CTime%20Class.md) or **TIMESTAMP_STRUCT**.|  
|[RFX_Double](../vs140/RFX_Double.md)|Transfers double-precision float data.|  
|[RFX_Int](../vs140/RFX_Int.md)|Transfers integer data.|  
|[RFX_Long](../vs140/RFX_Long.md)|Transfers long integer data.|  
|[RFX_LongBinary](../vs140/RFX_LongBinary.md)|Transfers binary large object (BLOB) data with an object of the [CLongBinary](../vs140/CLongBinary-Class.md) class.|  
|[RFX_Single](../vs140/RFX_Single.md)|Transfers float data.|  
|[RFX_Text](../vs140/RFX_Text.md)|Transfers string data.|  
  
### Bulk RFX Functions (ODBC)  
  
|||  
|-|-|  
|[RFX_Binary_Bulk](../vs140/RFX_Binary_Bulk.md)|Transfers arrays of byte data.|  
|[RFX_Bool_Bulk](../vs140/RFX_Bool_Bulk.md)|Transfers arrays of Boolean data.|  
|[RFX_Byte_Bulk](../vs140/RFX_Byte_Bulk.md)|Transfers arrays of single bytes.|  
|[RFX_Date_Bulk](../vs140/RFX_Date_Bulk.md)|Transfers arrays of data of type **TIMESTAMP_STRUCT**.|  
|[RFX_Double_Bulk](../vs140/RFX_Double_Bulk.md)|Transfers arrays of double-precision, floating-point data.|  
|[RFX_Int_Bulk](../vs140/RFX_Int_Bulk.md)|Transfers arrays of integer data.|  
|[RFX_Long_Bulk](../vs140/RFX_Long_Bulk.md)|Transfers arrays of long integer data.|  
|[RFX_Single_Bulk](../vs140/RFX_Single_Bulk.md)|Transfers arrays of floating-point data.|  
|[RFX_Text_Bulk](../vs140/RFX_Text_Bulk.md)|Transfers arrays of data of type **LPSTR**.|  
  
### DFX Functions (DAO)  
  
|||  
|-|-|  
|[DFX_Binary](../vs140/DFX_Binary.md)|Transfers arrays of bytes of type [CByteArray](../vs140/CByteArray-Class.md).|  
|[DFX_Bool](../vs140/DFX_Bool.md)|Transfers Boolean data.|  
|[DFX_Byte](../vs140/DFX_Byte.md)|Transfers a single byte of data.|  
|[DFX_Currency](../vs140/DFX_Currency.md)|Transfers currency data, of type [COleCurrency](../vs140/COleCurrency-Class.md).|  
|[DFX_DateTime](../vs140/DFX_DateTime.md)|Transfers time and date data, of type [COleDateTime](../vs140/COleDateTime-Class.md).|  
|[DFX_Double](../vs140/DFX_Double.md)|Transfers double-precision float data.|  
|[DFX_Long](../vs140/DFX_Long.md)|Transfers long integer data.|  
|[DFX_LongBinary](../vs140/DFX_LongBinary.md)|Transfers binary large object (BLOB) data with an object of the `CLongBinary` class. For DAO, it is recommended that you use [DFX_Binary](../vs140/DFX_Binary.md) instead.|  
|[DFX_Short](../vs140/DFX_Short.md)|Transfers short integer data.|  
|[DFX_Single](../vs140/DFX_Single.md)|Transfers float data.|  
|[DFX_Text](../vs140/DFX_Text.md)|Transfers string data.|  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CRecordset::DoFieldExchange](../vs140/CRecordset--DoFieldExchange.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)   
 [CDaoRecordset::DoFieldExchange](../vs140/CDaoRecordset--DoFieldExchange.md)