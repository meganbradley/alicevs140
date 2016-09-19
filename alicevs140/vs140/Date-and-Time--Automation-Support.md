---
title: "Date and Time: Automation Support"
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
ms.assetid: 6eee94c4-943d-4ffc-bf7c-bdda89337ab0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Date and Time: Automation Support
This article describes how to take advantage of the class library services related to date and time management. Procedures described include:  
  
-   [Getting the current time](../vs140/Current-Time--Automation-Classes.md)  
  
-   [Calculating elapsed time](../vs140/Elapsed-Time--Automation-Classes.md)  
  
-   [Formatting a string representation of a date/time](../vs140/Formatting-Time--Automation-Classes.md)  
  
 The [COleDateTime](../vs140/COleDateTime-Class.md) class provides a way to represent date and time information. It provides finer granularity and a greater range than the [CTime](../Topic/CTime%20Class.md) class. The [COleDateTimeSpan](../vs140/COleDateTimeSpan-Class.md) class represents elapsed time, such as the difference between two `COleDateTime` objects.  
  
 The `COleDateTime` and `COleDateTimeSpan` classes are designed to be used with the `COleVariant` class used in Automation. `COleDateTime` and `COleDateTimeSpan` are also useful in MFC database programming, but they can be used whenever you want to manipulate date and time values. Although the `COleDateTime` class has a greater range of values and finer granularity than the `CTime` class, it requires more storage per object than `CTime`. There are also some special considerations when working with the underlying **DATE** type. See [The DATE Type](../vs140/DATE-Type.md) for more details on the implementation of **DATE**.  
  
 `COleDateTime` objects can be used to represent dates between January 1, 100, and December 31, 9999. `COleDateTime` objects are floating point values, with an approximate resolution of 1 millisecond. `COleDateTime` is based on the **DATE** data type, defined in the MFC documentation under [COleDateTime::operator DATE](../vs140/COleDateTime--operator-DATE.md). The actual implementation of **DATE** extends beyond these bounds. The `COleDateTime` implementation imposes these bounds to facilitate working with the class.  
  
 `COleDateTime` does not support Julian dates. The Gregorian calendar is assumed to extend back in time to January 1, 100.  
  
 `COleDateTime` ignores Daylight Saving Time (DST). The following code example compares two methods of calculating a time span that crosses the DST switchover date: one using the CRT, and the other using `COleDateTime`. DST switches over, in most locales, in the second week in April and the third in October.  
  
 The first method sets two `CTime` objects, *time1* and *time2*, to April 5 and April 6 respectively, using the standard C type structures **tm** and `time_t`. The code displays *time1* and *time2* and the time span between them.  
  
 The second method creates two `COleDateTime` objects, `oletime1` and `oletime2`, and sets them to the same dates as *time1* and *time2*. It displays `oletime1` and `oletime2` and the time span between them.  
  
 The CRT correctly calculates a difference of 23 hours. `COleDateTimeSpan` calculates a difference of 24 hours.  
  
 Note that a workaround is used near the end of the example to display the date properly using `COleDateTime::Format`. See the Knowledge Base article "BUG: Format("%D") Fails for `COleDateTime` and `COleDateTimeSpan`" (Q167338).  
  
 [!CODE [NVC_ATLMFC_Utilities#176](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#176)]  
  
## See Also  
 [Date and Time](../vs140/Date-and-Time.md)