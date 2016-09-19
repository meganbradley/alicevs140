---
title: "COleDateTime::SetDate"
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
ms.assetid: 76e8466b-897a-4144-a545-4ccdc1bb035d
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::SetDate
Sets the date of this `COleDateTime` object.  
  
## Syntax  
  
```  
  
      int SetDate(  
   int nYear,  
   int nMonth,  
   int nDay   
) throw( );  
```  
  
#### Parameters  
 `nYear`, `nMonth`, `nDay`  
 Indicate the date components to be copied into this `COleDateTime` object.  
  
## Return Value  
 Zero if the value of this `COleDateTime` object was set successfully; otherwise, 1. This return value is based on the **DateTimeStatus** enumerated type. For more information, see the [SetStatus](../vs140/COleDateTime--SetStatus.md) member function.  
  
## Remarks  
 The date is set to the specified values. The time is set to time 0, midnight.  
  
 See the following table for bounds for the parameter values:  
  
|Parameter|Bounds|  
|---------------|------------|  
|`nYear`|100 – 9999|  
|`nMonth`|1 – 12|  
|`nDay`|0 – 31|  
  
 If the day of the month overflows, it is converted to the correct day of the next month and the month and/or year is incremented accordingly. A day value of zero indicates the last day of the previous month. The behavior is the same as `SystemTimeToVariantTime`.  
  
 If the date value specified by the parameters is not valid, the status of this object is set to **COleDateTime::invalid**. You should use [GetStatus](../vs140/COleDateTime--GetStatus.md) to check the validity of the **DATE** value and should not assume that the value of [m_dt](../vs140/COleDateTime--m_dt.md) will remain unmodified.  
  
 Here are some examples of date values:  
  
|`nYear`|`nMonth`|`nDay`|Value|  
|-------------|--------------|------------|-----------|  
|2000|2|29|29 February 2000|  
|1776|7|4|4 July 1776|  
|1925|4|35|35 April 1925 (invalid date)|  
|10000|1|1|1 January 10000 (invalid date)|  
  
 To set both date and time, see [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md).  
  
 For information on member functions that query the value of this `COleDateTime` object, see the following member functions:  
  
-   [GetDay](../vs140/COleDateTime--GetDay.md)  
  
-   [GetMonth](../vs140/COleDateTime--GetMonth.md)  
  
-   [GetYear](../vs140/COleDateTime--GetYear.md)  
  
-   [GetHour](../vs140/COleDateTime--GetHour.md)  
  
-   [GetMinute](../vs140/COleDateTime--GetMinute.md)  
  
-   [GetSecond](../vs140/COleDateTime--GetSecond.md)  
  
-   [GetDayOfWeek](../vs140/COleDateTime--GetDayOfWeek.md)  
  
-   [GetDayOfYear](../vs140/COleDateTime--GetDayOfYear.md)  
  
 For more information about the bounds for `COleDateTime` values, see the article [Date and Time: Automation Support](../vs140/Date-and-Time--Automation-Support.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#11](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#11)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)   
 [COleDateTime::m_dt](../vs140/COleDateTime--m_dt.md)