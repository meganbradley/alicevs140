---
title: "CDaoRecordset::FillCache"
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
ms.assetid: 0bca1482-c573-490b-9f5b-bb3ce79e946a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::FillCache
Call this member function to cache a specified number of records from the recordset.  
  
## Syntax  
  
```  
  
      void FillCache(  
   long* pSize = NULL,  
   COleVariant* pBookmark = NULL   
);  
```  
  
#### Parameters  
 `pSize`  
 Specifies the number of rows to fill in the cache. If you omit this parameter, the value is determined by the CacheSize property setting of the underlying DAO object.  
  
 `pBookmark`  
 A [COleVariant](../vs140/COleVariant-Class.md) specifying a bookmark. The cache is filled starting from the record indicated by this bookmark. If you omit this parameter, the cache is filled starting from the record indicated by the CacheStart property of the underlying DAO object.  
  
## Remarks  
 Caching improves the performance of an application that retrieves, or fetches, data from a remote server. A cache is space in local memory that holds the data most recently fetched from the server on the assumption that the data will probably be requested again while the application is running. When data is requested, the Microsoft Jet database engine checks the cache for the data first rather than fetching it from the server, which takes more time. Using data caching on non-ODBC data sources has no effect as the data is not saved in the cache.  
  
 Rather than waiting for the cache to be filled with records as they are fetched, you can explicitly fill the cache at any time by calling the `FillCache` member function. This is a faster way to fill the cache because `FillCache` fetches several records at once instead of one at a time. For example, while each screenful of records is being displayed, you can have your application call `FillCache` to fetch the next screenful of records.  
  
 Any ODBC database accessed with recordset objects can have a local cache. To create the cache, open a recordset object from the remote data source, and then call the `SetCacheSize` and `SetCacheStart` member functions of the recordset. If `lSize` and *lBookmark* create a range that is partly or wholly outside the range specified by `SetCacheSize` and `SetCacheStart`, the portion of the recordset outside this range is ignored and is not loaded into the cache. If `FillCache` requests more records than remain in the remote data source, only the remaining records are fetched, and no exception is thrown.  
  
 Records fetched from the cache do not reflect changes made concurrently to the source data by other users.  
  
 `FillCache` fetches only records not already cached. To force an update of all the cached data, call the `SetCacheSize` member function with an `lSize` parameter equal to 0, call `SetCacheSize` again with the `lSize` parameter equal to the size of the cache you originally requested, and then call `FillCache`.  
  
 For related information, see the topic "FillCache Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetCacheSize](../vs140/CDaoRecordset--GetCacheSize.md)   
 [CDaoRecordset::GetCacheStart](../vs140/CDaoRecordset--GetCacheStart.md)   
 [CDaoRecordset::SetCacheSize](../vs140/CDaoRecordset--SetCacheSize.md)   
 [CDaoRecordset::SetCacheStart](../vs140/CDaoRecordset--SetCacheStart.md)