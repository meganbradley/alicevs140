---
title: "CRecordset::GetBookmark"
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
ms.assetid: 14cff7c7-811b-4f93-8d9c-188707322fe6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::GetBookmark
Obtains the bookmark value for the current record.  
  
## Syntax  
  
```  
  
      void GetBookmark(   
   CDBVariant& varBookmark    
);  
```  
  
#### Parameters  
 `varBookmark`  
 A reference to a [CDBVariant](../vs140/CDBVariant-Class.md) object representing the bookmark on the current record.  
  
## Remarks  
 To determine if bookmarks are supported on the recordset, call [CanBookmark](../vs140/CRecordset--CanBookmark.md). To make bookmarks available if they are supported, you must set the **CRecordset::useBookmarks** option in the `dwOptions` parameter of the [Open](../vs140/CRecordset--Open.md) member function.  
  
> [!NOTE]
>  If bookmarks are unsupported or unavailable, calling `GetBookmark` will result in an exception being thrown. Bookmarks are not supported on forward-only recordsets.  
  
 `GetBookmark` assigns the value of the bookmark for the current record to a `CDBVariant` object. To return to that record at any time after moving to a different record, call [SetBookmark](../vs140/CRecordset--SetBookmark.md) with the corresponding `CDBVariant` object.  
  
> [!NOTE]
>  After certain recordset operations, bookmarks may no longer be valid. For example, if you call `GetBookmark` followed by **Requery**, you may not be able to return to the record with `SetBookmark`. Call [CDatabase::GetBookmarkPersistence](../vs140/CDatabase--GetBookmarkPersistence.md) to check whether you can safely call `SetBookmark`.  
  
 For more information about bookmarks and recordset navigation, see the articles [Recordset: Bookmarks and Absolute Positions (ODBC)](../vs140/Recordset--Bookmarks-and-Absolute-Positions--ODBC-.md) and [Recordset: Scrolling (ODBC)](../vs140/Recordset--Scrolling--ODBC-.md).  
  
## Exceptions  
 This method can throw exceptions of type **CDBException\*** and `CMemoryException*`.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::CanBookmark](../vs140/CRecordset--CanBookmark.md)   
 [CRecordset::SetBookmark](../vs140/CRecordset--SetBookmark.md)   
 [CDatabase::GetBookmarkPersistence](../vs140/CDatabase--GetBookmarkPersistence.md)