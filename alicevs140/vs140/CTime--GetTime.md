---
title: "CTime::GetTime"
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
ms.assetid: 82e9dc7e-c7d3-492b-a26c-c129613b4a81
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetTime
Returns a **__time64_t** value for the given `CTime` object.  
  
## Syntax  
  
```  
  
__time64_t GetTime( ) const throw( );  
```  
  
## Return Value  
 **GetTime** will return the number of seconds between the current `CTime` object and January 1, 1970.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#158](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#158)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTime::CTime](../Topic/CTime::CTime.md)