---
title: "COleDateTimeSpan::GetTotalDays"
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
ms.assetid: 997e2e29-fa67-4a9e-b2f0-962a19ee0413
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::GetTotalDays
Retrieves this date/time-span value expressed in days.  
  
## Syntax  
  
```  
  
double GetTotalDays( ) const throw( );  
  
```  
  
## Return Value  
 This date/time-span value expressed in days. Although this function is prototyped to return a double, it will always return an integer value.  
  
## Remarks  
 The return values from this function range between approximately – 3.65e6 and 3.65e6.  
  
 For other functions that query the value of a `COleDateTimeSpan` object, see the following member functions:  
  
-   [GetDays](../vs140/COleDateTimeSpan--GetDays.md)  
  
-   [GetHours](../vs140/COleDateTimeSpan--GetHours.md)  
  
-   [GetMinutes](../vs140/COleDateTimeSpan--GetMinutes.md)  
  
-   [GetSeconds](../vs140/COleDateTimeSpan--GetSeconds.md)  
  
-   [GetTotalHours](../vs140/COleDateTimeSpan--GetTotalHours.md)  
  
-   [GetTotalMinutes](../vs140/COleDateTimeSpan--GetTotalMinutes.md)  
  
-   [GetTotalSeconds](../vs140/COleDateTimeSpan--GetTotalSeconds.md)  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#20](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#20)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::SetDateTimeSpan](../vs140/COleDateTimeSpan--SetDateTimeSpan.md)   
 [COleDateTimeSpan::operator double](../vs140/COleDateTimeSpan--operator-double.md)