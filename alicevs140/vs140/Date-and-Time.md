---
title: "Date and Time"
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
ms.assetid: ecf56dc5-d418-4603-ad3e-af7e205a6403
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Date and Time
MFC supports several different ways of working with dates and times. These include:  
  
-   General-purpose time classes. The [CTime](../Topic/CTime%20Class.md) and [CTimeSpan](../vs140/CTimeSpan-Class.md) classes encapsulate most of the functionality associated with the ANSI-standard time library, which is declared in TIME.H.  
  
-   Support for system clock. With MFC version 3.0, support was added to `CTime` for the Win32 `SYSTEMTIME` and `FILETIME` data types.  
  
-   Support for the Automation [DATE data type](../vs140/DATE-Type.md). **DATE** supports date, time, and date/time values. The [COleDateTime](../vs140/COleDateTime-Class.md) and [COleDateTimeSpan](../vs140/COleDateTimeSpan-Class.md) classes encapsulate this functionality. They work with the [COleVariant](../vs140/COleVariant-Class.md) class using Automation support.  
  
## What do you want to know more about?  
  
-   [Date and Time: General-Purpose Classes](../vs140/Date-and-Time--General-Purpose-Classes.md)  
  
-   [Date and Time: SYSTEMTIME Support](../vs140/Date-and-Time--SYSTEMTIME-Support.md)  
  
-   [Date and Time: Automation Support](../vs140/Date-and-Time--Automation-Support.md)  
  
-   [Date and Time: Database Support](../vs140/Date-and-Time--Database-Support.md)  
  
## See Also  
 [Concepts](../vs140/MFC-Concepts.md)   
 [General MFC Topics](../vs140/General-MFC-Topics.md)