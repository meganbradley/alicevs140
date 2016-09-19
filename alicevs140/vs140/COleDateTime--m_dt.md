---
title: "COleDateTime::m_dt"
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
ms.assetid: 6c5a4c67-682f-4040-be19-634e55d8abe4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::m_dt
The underlying **DATE** structure for this `COleDateTime` object.  
  
## Syntax  
  
```  
  
DATE m_dt;  
  
```  
  
## Remarks  
  
> [!CAUTION]
>  Changing the value in the **DATE** object accessed by the pointer returned by this function will change the value of this `COleDateTime` object. It does not change the status of this `COleDateTime` object.  
  
 For more information about the implementation of the **DATE** object, see the article [Date and Time: Automation Support](../vs140/Date-and-Time--Automation-Support.md).  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::COleDateTime](../Topic/COleDateTime::COleDateTime.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::SetDate](../vs140/COleDateTime--SetDate.md)   
 [COleDateTime::SetTime](../vs140/COleDateTime--SetTime.md)   
 [COleDateTime::operator DATE](../vs140/COleDateTime--operator-DATE.md)