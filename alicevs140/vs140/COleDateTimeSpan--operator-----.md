---
title: "COleDateTimeSpan::operator +, -"
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
ms.assetid: f062d36d-5128-4967-8a51-0c580c2c80a4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan::operator +, -
Add, subtract, and change sign for `COleDateTimeSpan` values.  
  
## Syntax  
  
```  
  
      COleDateTimeSpan operator +(   
   const COleDateTimeSpan& dateSpan    
) const throw( );  
COleDateTimeSpan operator -(   
   const COleDateTimeSpan& dateSpan    
) const throw( );  
COleDateTimeSpan operator -( ) const throw( );  
```  
  
## Remarks  
 The first two operators let you add and subtract date/time-span values. The third lets you change the sign of a date/time-span value.  
  
 If either of the operands is null, the status of the resulting `COleDateTimeSpan` value is null.  
  
 If either of the operands is invalid and the other is not null, the status of the resulting `COleDateTimeSpan` value is invalid.  
  
 For more information on the valid, invalid, and null status values, see the [m_status](../vs140/COleDateTimeSpan--m_status.md) member variable.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#23](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#23)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTimeSpan::operator +=, -=](../vs140/COleDateTimeSpan--operator--=---=.md)