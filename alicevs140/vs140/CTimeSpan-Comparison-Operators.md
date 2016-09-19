---
title: "CTimeSpan Comparison Operators"
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
ms.assetid: a58a57c6-273a-4407-9f30-e96815801f9f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan Comparison Operators
Comparison operators.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   CTimeSpan span   
) const throw( );  
bool operator !=(  
   CTimeSpan span   
) const throw( );  
bool operator <(  
   CTimeSpan span   
) const throw( );  
bool operator >(  
   CTimeSpan span   
) const throw( );  
bool operator <=(  
   CTimeSpan span   
) const throw( );  
bool operator >=(  
   CTimeSpan span   
) const throw( );  
```  
  
#### Parameters  
 `span`  
  
 The object to compare.  
  
## Return Value  
 These operators compare two relative time values. They return **true** if the condition is true; otherwise **false**.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#169](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#169)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)