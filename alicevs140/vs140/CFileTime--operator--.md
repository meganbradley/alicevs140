---
title: "CFileTime::operator &gt;"
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
ms.assetid: 51910a08-64f8-4b52-9d21-4d0390d41845
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTime::operator &gt;
This operator compares two `CFileTime` objects to determine the larger.  
  
## Syntax  
  
```  
  
      bool operator >(  
   CFileTime ft   
) const throw( );  
```  
  
#### Parameters  
 `ft`  
 The `CFileTime` object to be compared.  
  
## Return Value  
 Returns **true** if the first object is greater than (later in time) than the second, otherwise **false**.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTime Class](../vs140/CFileTime-Class.md)