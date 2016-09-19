---
title: "CTime::operator +=, -="
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
ms.assetid: 703dd5e5-f15f-4ed7-a472-aae968d2948a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::operator +=, -=
These operators add and subtract a `CTimeSpan` object to and from this `CTime` object.  
  
## Syntax  
  
```  
  
      CTime& operator +=(  
   CTimeSpan span   
) throw( );  
CTime& operator -=(  
   CTimeSpan span   
) throw( );  
```  
  
#### Parameters  
 `span`  
 The `CTimeSpan` object to be added or subtracted.  
  
## Return Value  
 The updated `CTime` object.  
  
## Remarks  
 These operators allow you to add and subtract a `CTimeSpan` object to and from this `CTime` object.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#160](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#160)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)