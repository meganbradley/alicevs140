---
title: "CFileTime::UTCToLocal"
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
ms.assetid: 5240c254-3411-48f3-8801-0e2d37d7dc49
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::UTCToLocal
Call this method to convert time based on the Coordinated Universal Time (UTC) to local file time.  
  
## Syntax  
  
```  
  
CFileTime UTCToLocal( ) const throw( );  
  
```  
  
## Return Value  
 Returns a `CFileTime` object containing the time in local file time format.  
  
## Example  
 [!CODE [NVC_MFCFiles#42](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#42)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)   
 [CFileTime::LocalToUTC](../vs140/CFileTime--LocalToUTC.md)