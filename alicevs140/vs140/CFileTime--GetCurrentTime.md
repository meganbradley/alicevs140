---
title: "CFileTime::GetCurrentTime"
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
ms.assetid: f432db49-bb50-49e3-b1dd-ef56c600d3ed
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::GetCurrentTime
Call this static function to retrieve a `CFileTime` object that represents the current system date and time.  
  
## Syntax  
  
```  
  
static CFileTime GetCurrentTime( ) throw( );  
  
```  
  
## Return Value  
 Returns the current system date and time in Coordinated Universal Time (UTC) format.  
  
## Example  
 [!CODE [NVC_MFCFiles#41](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#41)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)   
 [time, _time32, _time64](../vs140/time--_time32--_time64.md)