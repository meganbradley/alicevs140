---
title: "CTimeSpan::operator +, -"
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
ms.assetid: ff974f5d-c68f-41ac-9ae3-53a76be47861
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan::operator +, -
Adds and subtracts `CTimeSpan` objects.  
  
## Syntax  
  
```  
  
      CTimeSpan operator +(  
   CTimeSpan span   
) const throw( );  
CTimeSpan operator -(  
   CTimeSpan span   
) const throw( );  
```  
  
#### Parameters  
 `span`  
 The value to add to the `CTimeSpan` object.  
  
## Return Value  
 A `CTimeSpan` object representing the result of the operation.  
  
## Remarks  
 These two operators allow you to add and subtract `CTimeSpan` objects to and from each other.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#167](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#167)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)