---
title: "CTime::GetMinute"
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
ms.assetid: c8ff0ec1-3521-4e49-9887-05f8a77f2c9c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetMinute
Returns the minute represented by the `CTime` object.  
  
## Syntax  
  
```  
  
int GetMinute( ) const throw( );  
```  
  
## Return Value  
 Returns the minute, based on local time, in the range 0 through 59.  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 See the example for [GetHour](../vs140/CTime--GetHour.md).  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)