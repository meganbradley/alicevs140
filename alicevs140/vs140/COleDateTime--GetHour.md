---
title: "COleDateTime::GetHour"
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
ms.assetid: d6d303a5-5f61-4ee5-a6bd-9cf012399c3a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetHour
Gets the hour represented by this date/time value.  
  
## Syntax  
  
```  
  
int GetHour( ) const throw( );  
  
```  
  
## Return Value  
 The hour represented by the value of this `COleDateTime` object or `COleDateTime::error` if the hour could not be obtained.  
  
## Remarks  
 Valid return values range between 0 and 23.  
  
 For information on other member functions that query the value of this `COleDateTime` object, see the following member functions:  
  
-   [GetDay](../vs140/COleDateTime--GetDay.md)  
  
-   [GetMonth](../vs140/COleDateTime--GetMonth.md)  
  
-   [GetYear](../vs140/COleDateTime--GetYear.md)  
  
-   [GetMinute](../vs140/COleDateTime--GetMinute.md)  
  
-   [GetSecond](../vs140/COleDateTime--GetSecond.md)  
  
-   [GetDayOfWeek](../vs140/COleDateTime--GetDayOfWeek.md)  
  
-   [GetDayOfYear](../vs140/COleDateTime--GetDayOfYear.md)  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#9](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#9)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)