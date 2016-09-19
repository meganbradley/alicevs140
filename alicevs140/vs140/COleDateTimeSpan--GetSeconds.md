---
title: "COleDateTimeSpan::GetSeconds"
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
ms.assetid: 17fc4e09-8912-42a3-9e08-695671f684e8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::GetSeconds
Retrieves the second portion of this date/time-span value.  
  
## Syntax  
  
```  
  
LONG GetSeconds( ) const throw( );  
  
```  
  
## Return Value  
 The seconds portion of this date/time-span value.  
  
## Remarks  
 The return values from this function range between – 59 and 59.  
  
 For other functions that query the value of a `COleDateTimeSpan` object, see the following member functions:  
  
-   [GetDays](../vs140/COleDateTimeSpan--GetDays.md)  
  
-   [GetHours](../vs140/COleDateTimeSpan--GetHours.md)  
  
-   [GetMinutes](../vs140/COleDateTimeSpan--GetMinutes.md)  
  
-   [GetTotalDays](../vs140/COleDateTimeSpan--GetTotalDays.md)  
  
-   [GetTotalHours](../vs140/COleDateTimeSpan--GetTotalHours.md)  
  
-   [GetTotalMinutes](../vs140/COleDateTimeSpan--GetTotalMinutes.md)  
  
-   [GetTotalSeconds](../vs140/COleDateTimeSpan--GetTotalSeconds.md)  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#19](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#19)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::SetDateTimeSpan](../vs140/COleDateTimeSpan--SetDateTimeSpan.md)