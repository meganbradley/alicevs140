---
title: "CTime::operator +, -"
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
ms.assetid: af3087f8-61ac-4987-b573-bff0fc13def3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::operator +, -
These operators add and subtract `CTimeSpan` and `CTime` objects.  
  
## Syntax  
  
```  
  
      CTime operator +(  
   CTimeSpan timeSpan   
) const throw( );  
CTime operator -(  
   CTimeSpan timeSpan   
) const throw( );  
CTimeSpan operator -(  
   CTime time   
) const throw( );  
```  
  
#### Parameters  
 *timeSpan*  
 The `CTimeSpan` object to be added or subtracted.  
  
 `time`  
 The `CTime` object to be subtracted.  
  
## Return Value  
 A `CTime` or `CTimeSpan` object representing the result of the operation.  
  
## Remarks  
 `CTime` objects represent absolute time, `CTimeSpan` objects represent relative time. The first two operators allow you to add and subtract `CTimeSpan` objects to and from `CTime` objects. The third operator allows you to subtract one `CTime` object from another to yield a `CTimeSpan` object.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#159](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#159)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)