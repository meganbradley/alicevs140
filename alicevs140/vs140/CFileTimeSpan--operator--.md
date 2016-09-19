---
title: "CFileTimeSpan::operator -"
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
ms.assetid: 0d066123-1cbb-488c-bfa3-c38a48efcf21
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTimeSpan::operator -
Performs subtraction on a **CFileTimeSpan** object.  
  
## Syntax  
  
```  
  
      CFileTimeSpan operator -(  
   CFileTimeSpan span   
) const throw( );  
```  
  
#### Parameters  
 `span`  
 A `CFileTimeSpan` object.  
  
## Return Value  
 Returns a `CFileTimeSpan` object representing the result of the difference between two time spans.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTimeSpan Class](../vs140/CFileTimeSpan-Class.md)