---
title: "COleDateTimeSpan Relational Operators"
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
ms.assetid: 147a0aee-8fab-444e-96cd-a54ddaff8fc6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTimeSpan Relational Operators
Comparison operators.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   const COleDateTimeSpan& dateSpan   
) const throw( );  
bool operator !=(  
   const COleDateTimeSpan& dateSpan   
) const throw( );  
bool operator <(  
   const COleDateTimeSpan& dateSpan   
) const throw( );  
bool operator >(  
   const COleDateTimeSpan& dateSpan   
) const throw( );  
bool operator <=(  
   const COleDateTimeSpan& dateSpan   
) const throw( );  
bool operator >=(  
   const COleDateTimeSpan& dateSpan   
) const throw( );  
```  
  
#### Parameters  
 *dateSpan*  
 The `COleDateTimeSpan` to compare.  
  
## Return Value  
 These operators compare two date/time-span values and return **true** if the condition is true; otherwise **false**.  
  
## Remarks  
  
> [!NOTE]
>  An ATLASSERT will occur if either operand is invalid.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#25](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#25)]  
  
 [!CODE [NVC_ATLMFC_Utilities#26](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#26)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTimeSpan Class](../vs140/COleDateTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)