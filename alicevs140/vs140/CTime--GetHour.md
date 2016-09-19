---
title: "CTime::GetHour"
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
ms.assetid: 916d0ee0-52e8-44b6-9035-093f1acd4151
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetHour
Returns the hour represented by the `CTime` object.  
  
## Syntax  
  
```  
  
int GetHour( ) const throw( );  
```  
  
## Return Value  
 Returns the hour, based on local time, in the range 0 through 23.  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#156](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#156)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)