---
title: "CTime::GetYear"
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
ms.assetid: f7f203a7-9356-45ff-9838-5af0480d1f83
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetYear
Returns the year represented by the `CTime` object.  
  
## Syntax  
  
```  
int GetYear( );  
```  
  
## Return Value  
 Returns the year, based on local time, in the range January 1,1970, to January 18, 2038 (inclusive).  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 See the example for [GetDay](../vs140/CTime--GetDay.md).  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTime::CTime](../Topic/CTime::CTime.md)