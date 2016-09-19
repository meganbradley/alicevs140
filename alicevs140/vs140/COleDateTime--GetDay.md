---
title: "COleDateTime::GetDay"
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
ms.assetid: 7441eadc-fcea-4d8d-827d-8953728559fc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetDay
Gets the day of the month represented by this date/time value.  
  
## Syntax  
  
```  
  
int GetDay( ) const throw( );  
  
```  
  
## Return Value  
 The day of the month represented by the value of this `COleDateTime` object or `COleDateTime::error` if the day could not be obtained.  
  
## Remarks  
 Valid return values range between 1 and 31.  
  
 For information on other member functions that query the value of this `COleDateTime` object, see the following member functions:  
  
-   [GetMonth](../vs140/COleDateTime--GetMonth.md)  
  
-   [GetYear](../vs140/COleDateTime--GetYear.md)  
  
-   [GetHour](../vs140/COleDateTime--GetHour.md)  
  
-   [GetMinute](../vs140/COleDateTime--GetMinute.md)  
  
-   [GetSecond](../vs140/COleDateTime--GetSecond.md)  
  
-   [GetDayOfWeek](../vs140/COleDateTime--GetDayOfWeek.md)  
  
-   [GetDayOfYear](../vs140/COleDateTime--GetDayOfYear.md)  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#6](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#6)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)