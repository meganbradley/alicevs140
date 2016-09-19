---
title: "CTime::GetDay"
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
ms.assetid: 777193bd-7420-4492-b925-8e881d2d60f4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetDay
Returns the day represent by the `CTime` object.  
  
## Syntax  
  
```  
  
int GetDay( ) const throw( );  
```  
  
## Return Value  
 Returns the day of the month, based on local time, in the range 1 through 31.  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal, statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#153](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#153)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTime::GetDayOfWeek](../vs140/CTime--GetDayOfWeek.md)