---
title: "CTime::GetDayOfWeek"
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
ms.assetid: a43c6a79-082a-480c-b451-5894e5ff097a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetDayOfWeek
Returns the day of the week represented by the `CTime` object.  
  
## Syntax  
  
```  
  
int GetDayOfWeek( ) const throw( );  
```  
  
## Return Value  
 Returns the day of the week based on local time; 1 = Sunday, 2 = Monday, to 7 = Saturday.  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#154](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#154)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)