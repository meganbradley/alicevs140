---
title: "CTimeSpan::GetDays"
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
ms.assetid: 8b7d65d6-41bb-441b-a9ef-c56f6eb80425
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan::GetDays
Returns a value that represents the number of complete days in this `CTimeSpan`.  
  
## Syntax  
  
```  
  
LONGLONG GetDays( ) const throw( );  
```  
  
## Return Value  
 Returns the number of complete 24-hour days in the time span. This value may be negative if the time span is negative.  
  
## Remarks  
 Note that Daylight Savings Time can cause `GetDays` to return a potentially surprising result. For example, when DST is in effect, **GetDays** reports the number of days between April 1 and May 1 as 29, not 30, because one day in April is shortened by an hour and therefore does not count as a complete day.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#164](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#164)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)