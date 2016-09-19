---
title: "CRecordset::SetBookmark"
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
ms.assetid: d8f2d1a2-2e4a-4300-901c-dccefae7ac4b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetBookmark
Positions the recordset on the record containing the specified bookmark.  
  
## Syntax  
  
```  
  
      void SetBookmark(   
   const CDBVariant& varBookmark    
);  
```  
  
#### Parameters  
 `varBookmark`  
 A reference to a [CDBVariant](../vs140/CDBVariant-Class.md) object containing the bookmark value for a specific record.  
  
## Remarks  
 To determine if bookmarks are supported on the recordset, call [CanBookmark](../vs140/CRecordset--CanBookmark.md). To make bookmarks available if they are supported, you must set the **CRecordset::useBookmarks** option in the `dwOptions` parameter of the [Open](../vs140/CRecordset--Open.md) member function.  
  
> [!NOTE]
>  If bookmarks are unsupported or unavailable, calling `SetBookmark` will result in an exception being thrown. Bookmarks are not supported on forward-only recordsets.  
  
 To first retrieve the bookmark for the current record, call [GetBookmark](../vs140/CRecordset--GetBookmark.md), which saves the bookmark value to a `CDBVariant` object. Later, you can return to that record by calling `SetBookmark` using the saved bookmark value.  
  
> [!NOTE]
>  After certain recordset operations, you should check the bookmark persistence before calling `SetBookmark`. For example, if you retrieve a bookmark with `GetBookmark` and then call **Requery**, the bookmark may no longer be valid. Call [CDatabase::GetBookmarkPersistence](../vs140/CDatabase--GetBookmarkPersistence.md) to check whether you can safely call `SetBookmark`.  
  
 For more information about bookmarks and recordset navigation, see the articles [Recordset: Bookmarks and Absolute Positions (ODBC)](../vs140/Recordset--Bookmarks-and-Absolute-Positions--ODBC-.md) and [Recordset: Scrolling (ODBC)](../vs140/Recordset--Scrolling--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::CanBookmark](../vs140/CRecordset--CanBookmark.md)   
 [CRecordset::GetBookmark](../vs140/CRecordset--GetBookmark.md)   
 [CRecordset::SetAbsolutePosition](../vs140/CRecordset--SetAbsolutePosition.md)   
 [CDatabase::GetBookmarkPersistence](../vs140/CDatabase--GetBookmarkPersistence.md)