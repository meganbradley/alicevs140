---
title: "COleDateTime::SetDateTime"
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
ms.assetid: e6157cd4-957d-40c9-bfbe-eb501c836b73
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::SetDateTime
Sets the date and time of this `COleDateTime` object.  
  
## Syntax  
  
```  
  
      int SetDateTime(  
   int nYear,  
   int nMonth,  
   int nDay,  
   int nHour,  
   int nMin,  
   int nSec   
) throw( );  
```  
  
#### Parameters  
 `nYear`, `nMonth`, `nDay`, `nHour`, `nMin`, `nSec`  
 Indicate the date and time components to be copied into this `COleDateTime` object.  
  
## Return Value  
 Zero if the value of this `COleDateTime` object was set successfully; otherwise, 1. This return value is based on the **DateTimeStatus** enumerated type. For more information, see the [SetStatus](../vs140/COleDateTime--SetStatus.md) member function.  
  
## Remarks  
 See the following table for bounds for the parameter values:  
  
|Parameter|Bounds|  
|---------------|------------|  
|`nYear`|100 – 9999|  
|`nMonth`|1 – 12|  
|`nDay`|0 – 31|  
|`nHour`|0 – 23|  
|`nMin`|0 – 59|  
|`nSec`|0 – 59|  
  
 If the day of the month overflows, it is converted to the correct day of the next month and the month and/or year is incremented accordingly. A day value of zero indicates the last day of the previous month. The behavior is the same as [SystemTimeToVariantTime](assetId:///d9d69521-9b33-4fc5-8a1c-929f216db450).  
  
 If the date or time value specified by the parameters is not valid, the status of this object is set to invalid and the value of this object is not changed.  
  
 Here are some examples of time values:  
  
|`nHour`|`nMin`|`nSec`|Value|  
|-------------|------------|------------|-----------|  
|1|3|3|01:03:03|  
|23|45|0|23:45:00|  
|25|30|0|Invalid|  
|9|60|0|Invalid|  
  
 Here are some examples of date values:  
  
|`nYear`|`nMonth`|`nDay`|Value|  
|-------------|--------------|------------|-----------|  
|1995|4|15|15 April 1995|  
|1789|7|14|17 July 1789|  
|1925|2|30|Invalid|  
|10000|1|1|Invalid|  
  
 To set the date only, see [COleDateTime::SetDate](../vs140/COleDateTime--SetDate.md). To set the time only, see [COleDateTime::SetTime](../vs140/COleDateTime--SetTime.md).  
  
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
 See the example for [GetStatus](../vs140/COleDateTime--GetStatus.md).  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDate](../vs140/COleDateTime--SetDate.md)   
 [COleDateTime::SetTime](../vs140/COleDateTime--SetTime.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)   
 [COleDateTime::m_dt](../vs140/COleDateTime--m_dt.md)