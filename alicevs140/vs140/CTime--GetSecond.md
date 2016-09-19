---
title: "CTime::GetSecond"
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
ms.assetid: ff58c967-9d21-4b99-ae45-c49571cba60a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetSecond
Returns the second represented by the `CTime` object.  
  
## Syntax  
  
```  
  
int GetSecond( ) const throw( );  
```  
  
## Return Value  
 Returns the second, based on local time, in the range 0 through 59.  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 See the example for [GetHour](../vs140/CTime--GetHour.md).  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)