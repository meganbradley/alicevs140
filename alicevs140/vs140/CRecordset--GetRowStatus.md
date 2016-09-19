---
title: "CRecordset::GetRowStatus"
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
ms.assetid: de62d535-b20a-414d-b551-8abb94dd6d9e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetRowStatus
Obtains the status for a row in the current rowset.  
  
## Syntax  
  
```  
  
      WORD GetRowStatus(  
   WORD wRow   
) const;  
```  
  
#### Parameters  
 `wRow`  
 The one-based position of a row in the current rowset. This value can range from 1 to the size of the rowset.  
  
## Return Value  
 A status value for the row. For details, see Remarks.  
  
## Remarks  
 `GetRowStatus` returns a value that indicates either any change in status to the row since it was last retrieved from the data source, or that no row corresponding to `wRow` was fetched. The following table lists the possible return values.  
  
|Status value|Description|  
|------------------|-----------------|  
|`SQL_ROW_SUCCESS`|The row is unchanged.|  
|`SQL_ROW_UPDATED`|The row has been updated.|  
|`SQL_ROW_DELETED`|The row has been deleted.|  
|`SQL_ROW_ADDED`|The row has been added.|  
|`SQL_ROW_ERROR`|The row is unretrievable due to an error.|  
|`SQL_ROW_NOROW`|There is no row that corresponds to `wRow`.|  
  
 For more information, see the ODBC API function **SQLExtendedFetch** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::CheckRowsetError](../vs140/CRecordset--CheckRowsetError.md)   
 [CRecordset::GetRowsFetched](../vs140/CRecordset--GetRowsFetched.md)   
 [CRecordset::RefreshRowset](../vs140/CRecordset--RefreshRowset.md)