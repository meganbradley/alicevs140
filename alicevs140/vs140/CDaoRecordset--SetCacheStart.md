---
title: "CDaoRecordset::SetCacheStart"
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
ms.assetid: baf13d1c-1dc9-4b42-88a4-a9c2982eb4c9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::SetCacheStart
Call this member function to specify the bookmark of the first record in the recordset to be cached.  
  
## Syntax  
  
```  
  
      void SetCacheStart(  
   COleVariant varBookmark   
);  
```  
  
#### Parameters  
 `varBookmark`  
 A [COleVariant](../vs140/COleVariant-Class.md) that specifies the bookmark of the first record in the recordset to be cached.  
  
## Remarks  
 You can use the bookmark value of any record for the `varBookmark` parameter of the `SetCacheStart` member function. Make the record you want to start the cache with the current record, establish a bookmark for that record using [SetBookmark](../vs140/CDaoRecordset--SetBookmark.md), and pass the bookmark value as the parameter for the `SetCacheStart` member function.  
  
 The Microsoft Jet database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.  
  
 Records retrieved from the cache do not reflect changes made concurrently to the source data by other users.  
  
 To force an update of all the cached data, pass the `lSize` parameter of `SetCacheSize` as 0, call `SetCacheSize` again with the size of the cache you originally requested, and then call the `FillCache` member function.  
  
 Note that if you are not creating a UNICODE recordset, the `COleVariant` object must be explicitly declared ANSI. This can be done by using the [COleVariant::COleVariant](../vs140/COleVariant--COleVariant.md)**(** `lpszSrc`**,** `vtSrc` **)** form of constructor with `vtSrc` set to `VT_BSTRT` (ANSI) or by using the **COleVariant** function [SetString](../vs140/COleVariant--SetString.md)**(** `lpszSrc`**,** `vtSrc` **)** with `vtSrc` set to `VT_BSTRT`.  
  
 For related information, see the topic CacheSize, CacheStart Properties" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::FillCache](../vs140/CDaoRecordset--FillCache.md)   
 [CDaoRecordset::GetCacheSize](../vs140/CDaoRecordset--GetCacheSize.md)   
 [CDaoRecordset::GetCacheStart](../vs140/CDaoRecordset--GetCacheStart.md)   
 [CDaoRecordset::SetCacheSize](../vs140/CDaoRecordset--SetCacheSize.md)