---
title: "COleDateTimeSpan::GetTotalMinutes"
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
ms.assetid: 1b9a530d-ca75-4c3a-b827-5349ef5ca969
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::GetTotalMinutes
Retrieves this date/time-span value expressed in minutes.  
  
## Syntax  
  
```  
  
double GetTotalMinutes( ) const throw( );  
  
```  
  
## Return Value  
 This date/time-span value expressed in minutes. Although this function is prototyped to return a double, it will always return an integer value.  
  
## Remarks  
 The return values from this function range between approximately – 5.26e9 and 5.26e9.  
  
 For other functions that query the value of a `COleDateTimeSpan` object, see the following member functions:  
  
-   [GetDays](../vs140/COleDateTimeSpan--GetDays.md)  
  
-   [GetHours](../vs140/COleDateTimeSpan--GetHours.md)  
  
-   [GetMinutes](../vs140/COleDateTimeSpan--GetMinutes.md)  
  
-   [GetSeconds](../vs140/COleDateTimeSpan--GetSeconds.md)  
  
-   [GetTotalDays](../vs140/COleDateTimeSpan--GetTotalDays.md)  
  
-   [GetTotalHours](../vs140/COleDateTimeSpan--GetTotalHours.md)  
  
-   [GetTotalSeconds](../vs140/COleDateTimeSpan--GetTotalSeconds.md)  
  
## Example  
 See the example for [GetTotalDays](../vs140/COleDateTimeSpan--GetTotalDays.md).  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::SetDateTimeSpan](../vs140/COleDateTimeSpan--SetDateTimeSpan.md)