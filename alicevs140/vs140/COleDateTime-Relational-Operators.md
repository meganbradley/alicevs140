---
title: "COleDateTime Relational Operators"
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
ms.assetid: 205c4fd0-5966-4e71-ad78-b8a4fd6777c9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime Relational Operators
Comparison operators.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   const COleDateTime& date   
) const throw( );  
bool operator !=(  
   const COleDateTime& date   
) const throw( );  
bool operator <(  
   const COleDateTime& date   
) const throw( );  
bool operator >(  
   const COleDateTime& date   
) const throw( );  
bool operator <=(  
   const COleDateTime& date   
) const throw( );  
bool operator >=(  
   const COleDateTime& date   
) const throw( );  
```  
  
#### Parameters  
 `date`  
 The **COleDateTime** object to be compared.  
  
## Return values  
 These operators compare two date/time values and return **true** if the condition is true; otherwise **false**.  
  
## Remarks  
  
> [!NOTE]
>  An ATLASSERT will occur if either of the two operands is invalid.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#13](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#13)]  
  
## Example  
 The operators **>=**, **<=**, **>**, and **<**, will assert if the `COleDateTime` object is set to null.  
  
 [!CODE [NVC_ATLMFC_Utilities#170](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#170)]  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)