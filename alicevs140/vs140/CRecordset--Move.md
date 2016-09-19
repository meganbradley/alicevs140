---
title: "CRecordset::Move"
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
ms.assetid: 2823a210-69f6-4f0a-a0fa-c2d5a98f0860
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::Move
Moves the current record pointer within the recordset, either forward or backward.  
  
## Syntax  
  
```  
  
      virtual void Move(   
   long nRows,   
   WORD wFetchType = SQL_FETCH_RELATIVE    
);  
```  
  
#### Parameters  
 `nRows`  
 The number of rows to move forward or backward. Positive values move forward, toward the end of the recordset. Negative values move backward, toward the beginning.  
  
 `wFetchType`  
 Determines the rowset that **Move** will fetch. For details, see Remarks.  
  
## Remarks  
 If you pass a value of 0 for `nRows`, **Move** refreshes the current record; **Move** will end any current `AddNew` or **Edit** mode, and will restore the current record's value before `AddNew` or **Edit** was called.  
  
> [!NOTE]
>  When you move through a recordset, you cannot skip deleted records. See [CRecordset::IsDeleted](../vs140/CRecordset--IsDeleted.md) for more information. When you open a `CRecordset` with the **skipDeletedRecords** option set, **Move** asserts if the `nRows` parameter is 0. This behavior prevents the refresh of rows that are deleted by other client applications using the same data. See the `dwOption` parameter in [Open](../vs140/CRecordset--Open.md) for a description of **skipDeletedRecords**.  
  
 **Move** repositions the recordset by rowsets. Based on the values for `nRows` and `wFetchType`, **Move** fetches the appropriate rowset and then makes the first record in that rowset the current record. If you have not implemented bulk row fetching, then the rowset size is always 1. When fetching a rowset, **Move** directly calls the [CheckRowsetError](../vs140/CRecordset--CheckRowsetError.md) member function to handle any errors resulting from the fetch.  
  
 Depending on the values you pass, **Move** is equivalent to other `CRecordset` member functions. In particular, the value of `wFetchType` may indicate a member function that is more intuitive and often the preferred method for moving the current record.  
  
 The following table lists the possible values for `wFetchType`, the rowset that **Move** will fetch based on `wFetchType` and `nRows`, and any equivalent member function corresponding to `wFetchType`.  
  
|wFetchType|Fetched rowset|Equivalent member function|  
|----------------|--------------------|--------------------------------|  
|`SQL_FETCH_RELATIVE` (the default value)|The rowset starting `nRows` row(s) from the first row in the current rowset.||  
|`SQL_FETCH_NEXT`|The next rowset; `nRows` is ignored.|[MoveNext](../vs140/CRecordset--MoveNext.md)|  
|`SQL_FETCH_PRIOR`|The previous rowset; `nRows` is ignored.|[MovePrev](../vs140/CRecordset--MovePrev.md)|  
|`SQL_FETCH_FIRST`|The first rowset in the recordset; `nRows` is ignored.|[MoveFirst](../vs140/CRecordset--MoveFirst.md)|  
|`SQL_FETCH_LAST`|The last complete rowset in the recordset; `nRows` is ignored.|[MoveLast](../vs140/CRecordset--MoveLast.md)|  
|`SQL_FETCH_ABSOLUTE`|If `nRows` > 0, the rowset starting `nRows` row(s) from the beginning of the recordset. If `nRows` < 0, the rowset starting `nRows` row(s) from the end of the recordset. If `nRows` = 0, then a beginning-of-file (BOF) condition is returned.|[SetAbsolutePosition](../vs140/CRecordset--SetAbsolutePosition.md)|  
|`SQL_FETCH_BOOKMARK`|The rowset starting at the row whose bookmark value corresponds to `nRows`.|[SetBookmark](../vs140/CRecordset--SetBookmark.md)|  
  
> [!NOTE]
>  For foward-only recordsets, **Move** is only valid with a value of `SQL_FETCH_NEXT` for `wFetchType`.  
  
> [!CAUTION]
>  Calling **Move** throws an exception if the recordset has no records. To determine whether the recordset has any records, call [IsBOF](../vs140/CRecordset--IsBOF.md) and [IsEOF](../vs140/CRecordset--IsEOF.md).  
  
> [!NOTE]
>  If you have scrolled past the beginning or end of the recordset (`IsBOF` or `IsEOF` returns nonzero), calling a **Move** function will possibly throw a `CDBException`. For example, if `IsEOF` returns nonzero and `IsBOF` does not, then `MoveNext` will throw an exception, but `MovePrev` will not.  
  
> [!NOTE]
>  If you call **Move** while the current record is being updated or added, the updates are lost without warning.  
  
 For more information about recordset navigation, see the articles [Recordset: Scrolling (ODBC)](../vs140/Recordset--Scrolling--ODBC-.md) and [Recordset: Bookmarks and Absolute Positions (ODBC)](../vs140/Recordset--Bookmarks-and-Absolute-Positions--ODBC-.md). For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md). For related information, see the ODBC API function **SQLExtendedFetch** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Example  
 [!CODE [NVC_MFCDatabase#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#28)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::MoveNext](../vs140/CRecordset--MoveNext.md)   
 [CRecordset::MovePrev](../vs140/CRecordset--MovePrev.md)   
 [CRecordset::MoveFirst](../vs140/CRecordset--MoveFirst.md)   
 [CRecordset::MoveLast](../vs140/CRecordset--MoveLast.md)   
 [CRecordset::SetAbsolutePosition](../vs140/CRecordset--SetAbsolutePosition.md)   
 [CRecordset::SetBookmark](../vs140/CRecordset--SetBookmark.md)   
 [CRecordset::IsBOF](../vs140/CRecordset--IsBOF.md)   
 [CRecordset::IsEOF](../vs140/CRecordset--IsEOF.md)   
 [CRecordset::CheckRowsetError](../vs140/CRecordset--CheckRowsetError.md)