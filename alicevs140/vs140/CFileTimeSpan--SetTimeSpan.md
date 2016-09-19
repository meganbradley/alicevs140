---
title: "CFileTimeSpan::SetTimeSpan"
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
ms.assetid: 9d1c948d-3833-4680-a928-eb3a56e9c9ba
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTimeSpan::SetTimeSpan
Call this method to set the time span of the `CFileTimeSpan` object.  
  
## Syntax  
  
```  
  
      void SetTimeSpan(  
   LONGLONG nSpan   
) throw( );  
```  
  
#### Parameters  
 `nSpan`  
 The new value for the time span in milliseconds.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTimeSpan Class](../vs140/CFileTimeSpan-Class.md)   
 [CFileTimeSpan::GetTimeSpan](../vs140/CFileTimeSpan--GetTimeSpan.md)