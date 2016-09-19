---
title: "CFileTime::LocalToUTC"
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
ms.assetid: 6a160476-1070-4471-b1a1-32e567b43f95
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::LocalToUTC
Call this method to convert a local file time to a file time based on the Coordinated Universal Time (UTC).  
  
## Syntax  
  
```  
  
CFileTime LocalToUTC( ) const throw( );  
  
```  
  
## Return Value  
 Returns a `CFileTime` object containing the time in UTC format.  
  
## Example  
 See the example for [CFileTime::UTCToLocal](../vs140/CFileTime--UTCToLocal.md).  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)   
 [CFileTime::UTCToLocal](../vs140/CFileTime--UTCToLocal.md)