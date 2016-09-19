---
title: "CFileTime::operator =="
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
ms.assetid: 6b4eb79b-e950-4471-bdab-64fa18f512d4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::operator ==
This operator compares two `CFileTime` objects for equality.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   CFileTime ft   
) const throw( );  
```  
  
#### Parameters  
 `ft`  
 The `CFileTime` object to compare.  
  
## Return Value  
 Returns **true** if the objects are equal, otherwise **false**.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)