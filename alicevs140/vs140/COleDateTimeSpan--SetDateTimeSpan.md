---
title: "COleDateTimeSpan::SetDateTimeSpan"
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
ms.assetid: 0587f1f5-b678-45b1-954c-3ea3fbc7f5fb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::SetDateTimeSpan
Sets the value of this date/time-span value.  
  
## Syntax  
  
```  
  
      void SetDateTimeSpan(   
   LONG lDays,   
   int nHours,   
   int nMins,   
   int nSecs    
) throw( );  
```  
  
#### Parameters  
 `lDays`, `nHours`, `nMins`, `nSecs`  
 Indicate the date-span and time-span values to be copied into this `COleDateTimeSpan` object.  
  
## Remarks  
 For functions that query the value of a `COleDateTimeSpan` object, see the following member functions:  
  
-   [GetDays](../vs140/COleDateTimeSpan--GetDays.md)  
  
-   [GetHours](../vs140/COleDateTimeSpan--GetHours.md)  
  
-   [GetMinutes](../vs140/COleDateTimeSpan--GetMinutes.md)  
  
-   [GetSeconds](../vs140/COleDateTimeSpan--GetSeconds.md)  
  
-   [GetTotalDays](../vs140/COleDateTimeSpan--GetTotalDays.md)  
  
-   [GetTotalHours](../vs140/COleDateTimeSpan--GetTotalHours.md)  
  
-   [GetTotalMinutes](../vs140/COleDateTimeSpan--GetTotalMinutes.md)  
  
-   [GetTotalSeconds](../vs140/COleDateTimeSpan--GetTotalSeconds.md)  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#21](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#21)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::GetStatus](../vs140/COleDateTimeSpan--GetStatus.md)   
 [COleDateTimeSpan::m_span](../vs140/COleDateTimeSpan--m_span.md)