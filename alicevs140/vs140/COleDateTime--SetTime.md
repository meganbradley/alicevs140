---
title: "COleDateTime::SetTime"
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
ms.assetid: bc6dadcf-d90d-4235-b791-82e7312ad7ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::SetTime
Sets the time of this `COleDateTime` object.  
  
## Syntax  
  
```  
  
      int SetTime(  
   int nHour,  
   int nMin,  
   int nSec   
) throw( );  
```  
  
#### Parameters  
 `nHour`, `nMin`, `nSec`  
 Indicate the time components to be copied into this `COleDateTime` object.  
  
## Return Value  
 Zero if the value of this `COleDateTime` object was set successfully; otherwise, 1. This return value is based on the **DateTimeStatus** enumerated type. For more information, see the [SetStatus](../vs140/COleDateTime--SetStatus.md) member function.  
  
## Remarks  
 The time is set to the specified values. The date is set to date 0, meaning 30 December 1899.  
  
 See the following table for bounds for the parameter values:  
  
|Parameter|Bounds|  
|---------------|------------|  
|`nHour`|0 – 23|  
|`nMin`|0 – 59|  
|`nSec`|0 – 59|  
  
 If the time value specified by the parameters is not valid, the status of this object is set to invalid and the value of this object is not changed.  
  
 Here are some examples of time values:  
  
|`nHour`|`nMin`|`nSec`|Value|  
|-------------|------------|------------|-----------|  
|1|3|3|01:03:03|  
|23|45|0|23:45:00|  
|25|30|0|Invalid|  
|9|60|0|Invalid|  
  
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
 See the example for [SetDate](../vs140/COleDateTime--SetDate.md).  
  
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