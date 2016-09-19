---
title: "COleDateTimeSpan::COleDateTimeSpan"
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
ms.assetid: 6bf5e93f-3485-4bdc-a669-52e818ed4dc0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::COleDateTimeSpan
Constructs a `COleDateTimeSpan` object.  
  
## Syntax  
  
```  
  
      COleDateTimeSpan( ) throw( );   
COleDateTimeSpan(  
   double dblSpanSrc   
) throw( );  
COleDateTimeSpan(   
   LONG lDays,   
   int nHours,   
   int nMins,   
   int nSecs    
) throw( );  
```  
  
#### Parameters  
 `dblSpanSrc`  
 The number of days to be copied into the new `COleDateTimeSpan` object.  
  
 `lDays`, `nHours`, `nMins`, `nSecs`  
 Indicate the day and time values to be copied into the new `COleDateTimeSpan` object.  
  
## Remarks  
 All of these constructors create new `COleDateTimeSpan` objects initialized to the specified value. A brief description of each of these constructors follows:  
  
-   **COleDateTimeSpan( )** Constructs a `COleDateTimeSpan` object initialized to 0.  
  
-   **COleDateTimeSpan(** `dblSpanSrc` **)** Constructs a `COleDateTimeSpan` object from a floating-point value.  
  
-   **COleDateTimeSpan(** `lDays`**,** `nHours`**,** `nMins`**,** `nSecs` **)** Constructs a `COleDateTimeSpan` object initialized to the specified numerical values.  
  
 The status of the new `COleDateTimeSpan` object is set to valid.  
  
 For more information about the bounds for `COleDateTimeSpan` values, see the article [Date and Time: Automation Support](../vs140/Date-and-Time--Automation-Support.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#14](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#14)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::operator =](../vs140/COleDateTimeSpan--operator-=.md)   
 [COleDateTimeSpan::GetStatus](../vs140/COleDateTimeSpan--GetStatus.md)   
 [COleDateTimeSpan::m_span](../vs140/COleDateTimeSpan--m_span.md)   
 [COleDateTimeSpan::m_status](../vs140/COleDateTimeSpan--m_status.md)