---
title: "CFileTimeSpan::operator &lt;="
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
ms.assetid: 0ff5ed10-3ef9-4796-9555-701429e5877e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTimeSpan::operator &lt;=
Compares two `CFileTimeSpan` objects to determine equality or the lesser.  
  
## Syntax  
  
```  
  
      bool operator<=(  
   CFileTimeSpan span   
) const throw( );  
```  
  
#### Parameters  
 `span`  
 The `CFileTimeSpan` object to be compared.  
  
## Return Value  
 Returns **true** if the first object is less than (that is, represents a shorter time period) or equal to the second, otherwise **false**.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTimeSpan Class](../vs140/CFileTimeSpan-Class.md)