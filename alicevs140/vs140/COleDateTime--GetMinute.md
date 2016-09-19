---
title: "COleDateTime::GetMinute"
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
ms.assetid: 26370967-45b4-4bbd-9cb6-09909510c00b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetMinute
Gets the minute represented by this date/time value.  
  
## Syntax  
  
```  
  
int GetMinute( ) const throw( );  
  
```  
  
## Return Value  
 The minute represented by the value of this `COleDateTime` object or `COleDateTime::error` if the minute could not be obtained.  
  
## Remarks  
 Valid return values range between 0 and 59.  
  
 For information on other member functions that query the value of this `COleDateTime` object, see the following member functions:  
  
-   [GetDay](../vs140/COleDateTime--GetDay.md)  
  
-   [GetMonth](../vs140/COleDateTime--GetMonth.md)  
  
-   [GetYear](../vs140/COleDateTime--GetYear.md)  
  
-   [GetHour](../vs140/COleDateTime--GetHour.md)  
  
-   [GetSecond](../vs140/COleDateTime--GetSecond.md)  
  
-   [GetDayOfWeek](../vs140/COleDateTime--GetDayOfWeek.md)  
  
-   [GetDayOfYear](../vs140/COleDateTime--GetDayOfYear.md)  
  
## Example  
 See the example for [GetHour](../vs140/COleDateTime--GetHour.md).  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)