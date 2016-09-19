---
title: "COleDateTimeSpan::m_span"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 8a25d18c-132d-4860-8283-c0733e3ceb71
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::m_span
The underlying **double** value for this `COleDateTime` object.  
  
## Syntax  
  
```  
  
double m_span;  
  
```  
  
## Remarks  
 This value expresses the date/time-span in days.  
  
> [!CAUTION]
>  Changing the value in the **double** data member will change the value of this `COleDateTimeSpan` object. It does not change the status of this `COleDateTimeSpan` object.  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::COleDateTimeSpan](../vs140/COleDateTimeSpan--COleDateTimeSpan.md)   
 [COleDateTimeSpan::SetDateTimeSpan](../vs140/COleDateTimeSpan--SetDateTimeSpan.md)   
 [COleDateTimeSpan::operator double](../vs140/COleDateTimeSpan--operator-double.md)