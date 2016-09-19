---
title: "CFileTime::operator -="
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
ms.assetid: 0f243532-05e3-4203-b381-b0badcc866b5
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::operator -=
This operator is used to perform subtraction on a `CFileTimeSpan` object and assign the result to the current object.  
  
## Syntax  
  
```  
  
      CFileTime& operator -=(  
   CFileTimeSpan span   
) throw( );  
```  
  
#### Parameters  
 `span`  
 A `CFileTimeSpan` object containing the relative time to subtract.  
  
## Return Value  
 Returns the updated `CFileTime` object.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)   
 [CFileTimeSpan Class](../vs140/CFileTimeSpan-Class.md)