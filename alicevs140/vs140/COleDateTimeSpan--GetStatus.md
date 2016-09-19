---
title: "COleDateTimeSpan::GetStatus"
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
ms.assetid: b90e9b9c-5ae2-41a4-97db-b2b85638a6ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::GetStatus
Gets the status (validity) of this `COleDateTimeSpan` object.  
  
## Syntax  
  
```  
  
DateTimeSpanStatus GetStatus( ) const throw( );  
  
```  
  
## Return Value  
 The status of this `COleDateTimeSpan` value.  
  
## Remarks  
 The return value is defined by the **DateTimeSpanStatus** enumerated type, which is defined within the `COleDateTimeSpan` class.  
  
 `enum DateTimeSpanStatus{`  
  
 `valid = 0,`  
  
 `invalid = 1,`  
  
 `null = 2,`  
  
 `};`  
  
 For a brief description of these status values, see the following list:  
  
-   **COleDateTimeSpan::valid** Indicates that this `COleDateTimeSpan` object is valid.  
  
-   **COleDateTimeSpan::invalid** Indicates that this `COleDateTimeSpan` object is invalid; that is, its value may be incorrect.  
  
-   **COleDateTimeSpan::null** Indicates that this `COleDateTimeSpan` object is null, that is, that no value has been supplied for this object. (This is "null" in the database sense of "having no value," as opposed to the C++ **NULL**.)  
  
 The status of a `COleDateTimeSpan` object is invalid in the following cases:  
  
-   If this object has experienced an overflow or underflow during an arithmetic assignment operation, namely, `+=` or `-=`.  
  
-   If an invalid value was assigned to this object.  
  
-   If the status of this object was explicitly set to invalid using `SetStatus`.  
  
 For more information about the operations that may set the status to invalid, see [COleDateTimeSpan::operator +, -](../vs140/COleDateTime--operator-----.md) and [COleDateTimeSpan::operator +=, -=](../vs140/COleDateTime--operator--=---=.md).  
  
 For more information about the bounds for `COleDateTimeSpan` values, see the article [Date and Time: Automation Support](../vs140/Date-and-Time--Automation-Support.md).  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::SetStatus](../vs140/COleDateTimeSpan--SetStatus.md)   
 [COleDateTimeSpan::m_status](../vs140/COleDateTimeSpan--m_status.md)