---
title: "CDaoRecordset::GetCacheStart"
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
ms.assetid: 0be13185-5326-4be5-8095-ed8776391747
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetCacheStart
Call this member function to obtain the bookmark value of the first record in the recordset to be cached.  
  
## Syntax  
  
```  
  
COleVariant GetCacheStart( );  
  
```  
  
## Return Value  
 A `COleVariant` that specifies the bookmark of the first record in the recordset to be cached.  
  
## Remarks  
 The Microsoft Jet database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.  
  
> [!NOTE]
>  Records retrieved from the cache do not reflect changes made concurrently to the source data by other users.  
  
 For related information, see the topic "CacheSize, CacheStart Properties" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::FillCache](../vs140/CDaoRecordset--FillCache.md)   
 [CDaoRecordset::GetCacheSize](../vs140/CDaoRecordset--GetCacheSize.md)   
 [CDaoRecordset::SetCacheSize](../vs140/CDaoRecordset--SetCacheSize.md)   
 [CDaoRecordset::SetCacheStart](../vs140/CDaoRecordset--SetCacheStart.md)