---
title: "COleDateTime::GetDayOfYear"
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
ms.assetid: 663dbbf2-7661-44c6-8d67-68ec2360efef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetDayOfYear
Gets the day of the year represented by this date/time value.  
  
## Syntax  
  
```  
  
int GetDayOfYear( ) const throw( );  
  
```  
  
## Return Value  
 The day of the year represented by the value of this `COleDateTime` object or `COleDateTime::error` if the day of the year could not be obtained.  
  
## Remarks  
 Valid return values range between 1 and 366, where January 1 = 1.  
  
 For information on other member functions that query the value of this `COleDateTime` object, see the following member functions:  
  
-   [GetDay](../vs140/COleDateTime--GetDay.md)  
  
-   [GetMonth](../vs140/COleDateTime--GetMonth.md)  
  
-   [GetYear](../vs140/COleDateTime--GetYear.md)  
  
-   [GetHour](../vs140/COleDateTime--GetHour.md)  
  
-   [GetMinute](../vs140/COleDateTime--GetMinute.md)  
  
-   [GetSecond](../vs140/COleDateTime--GetSecond.md)  
  
-   [GetDayOfWeek](../vs140/COleDateTime--GetDayOfWeek.md)  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#8](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#8)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)