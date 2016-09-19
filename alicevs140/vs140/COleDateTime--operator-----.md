---
title: "COleDateTime::operator +, -"
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
ms.assetid: fb8a99e5-9292-40fc-a5c1-d489d96b931c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::operator +, -
Add and subtract **ColeDateTime** values.  
  
## Syntax  
  
```  
  
      COleDateTime operator +(  
   COleDateTimeSpan dateSpan   
) const throw( );  
COleDateTime operator -(  
   COleDateTimeSpan dateSpan   
) const throw( );  
COleDateTimeSpan operator -(  
   const COleDateTime& date   
) const throw( );  
```  
  
## Remarks  
 `COleDateTime` objects represent absolute times. [COleDateTimeSpan](../vs140/COleDateTimeSpan-Class.md) objects represent relative times. The first two operators allow you to add and subtract a `COleDateTimeSpan` value from a `COleDateTime` value. The third operator allows you to subtract one `COleDateTime` value from another to yield a `COleDateTimeSpan` value.  
  
 If either of the operands is null, the status of the resulting `COleDateTime` value is null.  
  
 If the resulting `COleDateTime` value falls outside the bounds of acceptable values, the status of that `COleDateTime` value is invalid.  
  
 If either of the operands is invalid and the other is not null, the status of the resulting `COleDateTime` value is invalid.  
  
 The **+** and **-** operators will assert if the `COleDateTime` object is set to null. See [COleDateTime Relational Operators](../vs140/COleDateTime-Relational-Operators.md) for an example.  
  
 For more information on the valid, invalid, and null status values, see the [m_status](../vs140/COleDateTime--m_status.md) member variable.  
  
 For more information about the bounds for `COleDateTime` values, see the article [Date and Time: Automation Support](../vs140/Date-and-Time--Automation-Support.md).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#12](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#12)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::operator +=, -=](../vs140/COleDateTime--operator--=---=.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)   
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)