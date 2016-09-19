---
title: "CDBException::m_nRetCode"
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
ms.topic: reference
ms.assetid: c66adbbf-e339-466e-9ca9-cf0614b94b9a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBException::m_nRetCode
Contains an ODBC error code of type **RETCODE** returned by an ODBC application programming interface (API) function.  
  
## Remarks  
 This type includes SQL-prefixed codes defined by ODBC and AFX_SQL-prefixed codes defined by the database classes. For a `CDBException`, this member will contain one of the following values:  
  
-   **AFX_SQL_ERROR_API_CONFORMANCE** The driver for a `CDatabase::OpenEx` or `CDatabase::Open` call does not conform to required ODBC API Conformance level 1 (**SQL_OAC_LEVEL1**).  
  
-   **AFX_SQL_ERROR_CONNECT_FAIL** Connection to the data source failed. You passed a **NULL** `CDatabase` pointer to your recordset constructor and the subsequent attempt to create a connection based on `GetDefaultConnect` failed.  
  
-   **AFX_SQL_ERROR_DATA_TRUNCATED** You requested more data than you have provided storage for. For information on increasing the provided data storage for `CString` or `CByteArray` data types, see the `nMaxLength` argument for [RFX_Text](../vs140/RFX_Text.md) and [RFX_Binary](../vs140/RFX_Binary.md) under "Macros and Globals."  
  
-   **AFX_SQL_ERROR_DYNASET_NOT_SUPPORTED** A call to `CRecordset::Open` requesting a dynaset failed. Dynasets are not supported by the driver.  
  
-   **AFX_SQL_ERROR_EMPTY_COLUMN_LIST** You attempted to open a table (or what you gave could not be identified as a procedure call or **SELECT** statement) but there are no columns identified in record field exchange (RFX) function calls in your `DoFieldExchange` override.  
  
-   **AFX_SQL_ERROR_FIELD_SCHEMA_MISMATCH** The type of an RFX function in your `DoFieldExchange` override is not compatible with the column data type in the recordset.  
  
-   **AFX_SQL_ERROR_ILLEGAL_MODE** You called `CRecordset::Update` without previously calling `CRecordset::AddNew` or `CRecordset::Edit`.  
  
-   **AFX_SQL_ERROR_LOCK_MODE_NOT_SUPPORTED** Your request to lock records for update could not be fulfilled because your ODBC driver does not support locking.  
  
-   **AFX_SQL_ERROR_MULTIPLE_ROWS_AFFECTED** You called `CRecordset::Update` or **Delete** for a table with no unique key and changed multiple records.  
  
-   **AFX_SQL_ERROR_NO_CURRENT_RECORD** You attempted to edit or delete a previously deleted record. You must scroll to a new current record after a deletion.  
  
-   **AFX_SQL_ERROR_NO_POSITIONED_UPDATES** Your request for a dynaset could not be fulfilled because your ODBC driver does not support positioned updates.  
  
-   **AFX_SQL_ERROR_NO_ROWS_AFFECTED** You called `CRecordset::Update` or **Delete**, but when the operation began the record could no longer be found.  
  
-   **AFX_SQL_ERROR_ODBC_LOAD_FAILED** An attempt to load the ODBC.DLL failed; Windows could not find or could not load this DLL. This error is fatal.  
  
-   **AFX_SQL_ERROR_ODBC_V2_REQUIRED** Your request for a dynaset could not be fulfilled because a Level 2-compliant ODBC driver is required.  
  
-   **AFX_SQL_ERROR_RECORDSET_FORWARD_ONLY** An attempt to scroll did not succeed because the data source does not support backward scrolling.  
  
-   **AFX_SQL_ERROR_SNAPSHOT_NOT_SUPPORTED** A call to `CRecordset::Open` requesting a snapshot failed. Snapshots are not supported by the driver. (This should only occur when the ODBC cursor library — ODBCCURS.DLL — is not present.)  
  
-   **AFX_SQL_ERROR_SQL_CONFORMANCE** The driver for a `CDatabase::OpenEx` or `CDatabase::Open` call does not conform to the required ODBC SQL Conformance level of "Minimum" (**SQL_OSC_MINIMUM**).  
  
-   **AFX_SQL_ERROR_SQL_NO_TOTAL** The ODBC driver was unable to specify the total size of a `CLongBinary` data value. The operation probably failed because a global memory block could not be preallocated.  
  
-   **AFX_SQL_ERROR_RECORDSET_READONLY** You attempted to update a read-only recordset, or the data source is read-only. No update operations can be performed with the recordset or the `CDatabase` object it is associated with.  
  
-   **SQL_ERROR** Function failed. The error message returned by the ODBC function **SQLError** is stored in the **m_strError** data member.  
  
-   **SQL_INVALID_HANDLE** Function failed due to an invalid environment handle, connection handle, or statement handle. This indicates a programming error. No additional information is available from the ODBC function **SQLError**.  
  
 The SQL-prefixed codes are defined by ODBC. The AFX-prefixed codes are defined in AFXDB.H, found in MFC\INCLUDE.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDBException Class](../vs140/CDBException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [CLongBinary Class](../vs140/CLongBinary-Class.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)