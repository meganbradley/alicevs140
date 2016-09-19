---
title: "CRowset::MoveToBookmark"
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
ms.assetid: 90124723-8daf-4692-ae2f-0db26b5db920
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::MoveToBookmark
Fetches the row marked by a bookmark or the row at a specified offset (`lSkip`) from that bookmark.  
  
## Syntax  
  
```  
  
      HRESULT MoveToBookmark(   
   const CBookmarkBase& bookmark,   
   LONG lSkip = 0    
) throw( );  
```  
  
#### Parameters  
 `bookmark`  
 [in] A bookmark marking the location from which you want to fetch data.  
  
 `lSkip`  
 [in] The number count of rows from the bookmark to the target row. If `lSkip` is zero, the first row fetched is the bookmarked row. If `lSkip` is 1, the first row fetched is the row after the bookmarked row. If `lSkip` is –1, the first row fetched is the row before the bookmarked row.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method requires the optional interface `IRowsetLocate`, which might not be supported on all providers; if this is the case, the method returns **E_NOINTERFACE**. You must also set **DBPROP_IRowsetLocate** to `VARIANT_TRUE` and set **DBPROP_CANFETCHBACKWARDS** to `VARIANT_TRUE` before calling **Open** on the table or command containing the rowset.  
  
 For information about using bookmarks in consumers, see [Using Bookmarks](../vs140/Using-Bookmarks.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)   
 [CRowset::MoveNext](../vs140/CRowset--MoveNext.md)   
 [CRowset::MoveFirst](../vs140/CRowset--MoveFirst.md)   
 [IRowsetLocate::GetRowsAt](https://msdn.microsoft.com/en-us/library/ms723031.aspx)   
 [CRowset::MovePrev](../vs140/CRowset--MovePrev.md)   
 [CRowset::MoveLast](../vs140/CRowset--MoveLast.md)