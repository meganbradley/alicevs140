---
title: "CRecordset::CheckRowsetError"
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
ms.assetid: ad1e0895-c903-4594-b24a-95144f310c03
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::CheckRowsetError
Called to handle errors generated during record fetching.  
  
## Syntax  
  
```  
  
      virtual void CheckRowsetError(   
   RETCODE nRetCode    
);  
```  
  
#### Parameters  
 `nRetCode`  
 An ODBC API function return code. For details, see Remarks.  
  
## Remarks  
 This virtual member function handles errors that occur when records are fetched, and is useful during bulk row fetching. You may want to consider overriding `CheckRowsetError` to implement your own error handling.  
  
 `CheckRowsetError` is called automatically in a cursor navigation operation, such as **Open**, **Requery**, or any **Move** operation. It is passed the return value of the ODBC API function **SQLExtendedFetch**. The following table lists the possible values for the `nRetCode` parameter.  
  
|nRetCode|Description|  
|--------------|-----------------|  
|**SQL_SUCCESS**|Function completed successfully; no additional information is available.|  
|**SQL_SUCCESS_WITH_INFO**|Function completed successfully, possibly with a nonfatal error. Additional information can be obtained by calling **SQLError**.|  
|**SQL_NO_DATA_FOUND**|All rows from the result set have been fetched.|  
|**SQL_ERROR**|Function failed. Additional information can be obtained by calling **SQLError**.|  
|**SQL_INVALID_HANDLE**|Function failed due to an invalid environment handle, connection handle, or statement handle. This indicates a programming error. No additional information is available from **SQLError**.|  
|`SQL_STILL_EXECUTING`|A function that was started asynchronously is still executing. Note that by default, MFC will never pass this value to `CheckRowsetError`; MFC will continue calling **SQLExtendedFetch** until it no longer returns `SQL_STILL_EXECUTING`.|  
  
 For more information about **SQLError**, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\***.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)   
 [CRecordset::GetRowsetSize](../vs140/CRecordset--GetRowsetSize.md)   
 [CRecordset::SetRowsetSize](../vs140/CRecordset--SetRowsetSize.md)   
 [CRecordset::Move](../vs140/CRecordset--Move.md)