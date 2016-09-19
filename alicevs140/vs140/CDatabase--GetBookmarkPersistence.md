---
title: "CDatabase::GetBookmarkPersistence"
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
ms.assetid: 568db51f-b026-4b73-944f-835ca9e6cecd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::GetBookmarkPersistence
Call this member function to determine the persistence of bookmarks on a recordset object after certain operations.  
  
## Syntax  
  
```  
  
DWORD GetBookmarkPersistence( ) const;  
  
```  
  
## Return Value  
 A bitmask that identifies the operations through which bookmarks persist on a recordset object. For details, see Remarks.  
  
## Remarks  
 For example, if you call `CRecordset::GetBookmark` and then call `CRecordset::Requery`, the bookmark obtained from `GetBookmark` may no longer be valid. You should call `GetBookmarkPersistence` before calling `CRecordset::SetBookmark`.  
  
 The following table lists the bitmask values that can be combined for the return value of `GetBookmarkPersistence`.  
  
|Bitmask value|Bookmark persistence|  
|-------------------|--------------------------|  
|`SQL_BP_CLOSE`|Bookmarks are valid after a **Requery** operation.|  
|`SQL_BP_DELETE`|The bookmark for a row is valid after a **Delete** operation on that row.|  
|`SQL_BP_DROP`|Bookmarks are valid after a **Close** operation.|  
|`SQL_BP_SCROLL`|Bookmarks are valid after any **Move** operation. This simply identifies if bookmarks are supported on the recordset, as returned by `CRecordset::CanBookmark`.|  
|`SQL_BP_TRANSACTION`|Bookmarks are valid after a transaction is committed or rolled back.|  
|`SQL_BP_UPDATE`|The bookmark for a row is valid after an **Update** operation on that row.|  
|`SQL_BP_OTHER_HSTMT`|Bookmarks associated with one recordset object are valid on a second recordset.|  
  
 For more information about this return value, see the ODBC API function **SQLGetInfo** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information about bookmarks, see the article [Recordset: Bookmarks and Absolute Positions (ODBC)](../vs140/Recordset--Bookmarks-and-Absolute-Positions--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [CRecordset::CanBookmark](../vs140/CRecordset--CanBookmark.md)   
 [CRecordset::GetBookmark](../vs140/CRecordset--GetBookmark.md)   
 [CRecordset::SetBookmark](../vs140/CRecordset--SetBookmark.md)