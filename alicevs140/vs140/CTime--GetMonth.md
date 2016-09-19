---
title: "CTime::GetMonth"
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
ms.assetid: b2b71fb9-b57b-4d2d-880d-a62ebbc4fd41
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetMonth
Returns the month represented by the `CTime` object.  
  
## Syntax  
  
```  
  
int GetMonth( ) const throw( );  
```  
  
## Return Value  
 Returns the month, based on local time, in the range 1 through 12 (1 = January).  
  
## Remarks  
 This function calls `GetLocalTm`, which uses an internal statically allocated buffer. The data in this buffer is overwritten because of calls to other `CTime` member functions.  
  
## Example  
 See the example for [GetDay](../vs140/CTime--GetDay.md).  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)