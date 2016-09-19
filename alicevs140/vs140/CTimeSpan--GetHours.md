---
title: "CTimeSpan::GetHours"
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
ms.assetid: e4cfb702-d981-4405-9f9f-80c04c1af28b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan::GetHours
Returns a value that represents the number of hours in the current day (–23 through 23).  
  
## Syntax  
  
```  
  
LONG GetHours( ) const throw( );  
```  
  
## Return Value  
 Returns the number of hours in the current day. The range is –23 through 23.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#165](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#165)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)