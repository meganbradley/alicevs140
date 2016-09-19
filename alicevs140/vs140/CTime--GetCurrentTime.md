---
title: "CTime::GetCurrentTime"
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
ms.assetid: 17a539d6-6f01-4cee-beeb-c9ea7b036adb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetCurrentTime
Returns a `CTime` object that represents the current time.  
  
## Syntax  
  
```  
  
static CTime WINAPI GetCurrentTime( ) throw( );  
```  
  
## Remarks  
 Returns the current system date and time in Coordinated Universal Time (UTC).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#152](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#152)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)