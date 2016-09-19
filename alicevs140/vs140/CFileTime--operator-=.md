---
title: "CFileTime::operator ="
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
ms.assetid: 2be57771-83bf-4f35-85b3-c3d736033bfd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::operator =
The assignment operator.  
  
## Syntax  
  
```  
  
      CFileTime& operator =(  
   const FILETIME& ft   
) throw( );  
```  
  
#### Parameters  
 `ft`  
 A `CFileTime` object containing the new time and date.  
  
## Return Value  
 Returns the updated `CFileTime` object.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)