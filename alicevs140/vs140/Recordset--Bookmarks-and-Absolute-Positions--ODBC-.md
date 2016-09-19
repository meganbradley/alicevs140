---
title: "Recordset: Bookmarks and Absolute Positions (ODBC)"
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
ms.assetid: 189788d6-33c1-41c5-9265-97db2a5d43cc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recordset: Bookmarks and Absolute Positions (ODBC)
This topic applies to the MFC ODBC classes.  
  
 When navigating through a recordset, you often need a way of returning to a particular record. A record's bookmark and absolute position provide two such methods.  
  
 This topic explains:  
  
-   [How to use bookmarks](#_core_bookmarks_in_mfc_odbc).  
  
-   [How to set the current record using absolute positions](#_core_absolute_positions_in_mfc_odbc).  
  
##  <a name="_core_bookmarks_in_mfc_odbc"></a> Bookmarks in MFC ODBC  
 A bookmark uniquely identifies a record. When you navigate through a recordset, you cannot always rely on the absolute position of a record because records can be deleted from the recordset. The reliable way to keep track of the position of a record is to use its bookmark. Class `CRecordset` supplies member functions for:  
  
-   Getting the bookmark of the current record, so you can save it in a variable ([GetBookmark](../vs140/CRecordset--GetBookmark.md)).  
  
-   Moving quickly to a given record by specifying its bookmark, which you saved earlier in a variable ([SetBookmark](../vs140/CRecordset--SetBookmark.md)).  
  
 The following example illustrates how to use these member functions to mark the current record and later return to it:  
  
```  
// rs is a CRecordset or  
// CRecordset-derived object  
  
CDBVariant varRecordToReturnTo;  
rs.GetBookmark( varRecordToReturnTo );  
  
// More code in which you  
// move to other records  
  
rs.SetBookmark( varRecordToReturnTo );  
```  
  
 You do not need to extract the underlying data type from the [CDBVariant Class](../vs140/CDBVariant-Class.md) object. Assign the value with `GetBookmark` and return to that bookmark with `SetBookmark`.  
  
> [!NOTE]
>  Depending on your ODBC driver and recordset type, bookmarks might not be supported. You can easily determine whether bookmarks are supported by calling [CRecordset::CanBookmark](../vs140/CRecordset--CanBookmark.md). Furthermore, if bookmarks are supported, you must explicitly choose to implement them by specifying the **CRecordset::useBookmarks** option in the [CRecordset::Open](../vs140/CRecordset--Open.md) member function. You should also check the persistence of bookmarks after certain recordset operations. For example, if you **Requery** a recordset, bookmarks might no longer be valid. Call [CDatabase::GetBookmarkPersistence](../vs140/CDatabase--GetBookmarkPersistence.md) to check whether you can safely call `SetBookmark`.  
  
##  <a name="_core_absolute_positions_in_mfc_odbc"></a> Absolute Positions in MFC ODBC  
 Besides bookmarks, class `CRecordset` allows you to set the current record by specifying an ordinal position. This is called absolute positioning.  
  
> [!NOTE]
>  Absolute positioning is not available on forward-only recordsets. For more information about forward-only recordsets, see [Recordset (ODBC)](../vs140/Recordset--ODBC-.md).  
  
 To move the current record pointer using absolute position, call [CRecordset::SetAbsolutePosition](../vs140/CRecordset--SetAbsolutePosition.md). When you pass a value to `SetAbsolutePosition`, the record corresponding to that ordinal position becomes the current record.  
  
> [!NOTE]
>  The absolute position of a record is potentially unreliable. If the user deletes records from the recordset, the ordinal position of any subsequent record changes. Bookmarks are the recommended method for moving the current record. For more information, see [Bookmarks in MFC ODBC](#_core_bookmarks_in_mfc_odbc).  
  
 For more information about recordset navigation, see [Recordset: Scrolling (ODBC)](../vs140/Recordset--Scrolling--ODBC-.md).  
  
## See Also  
 [Recordset (ODBC)](../vs140/Recordset--ODBC-.md)