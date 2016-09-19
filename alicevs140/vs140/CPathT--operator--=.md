---
title: "CPathT::operator +="
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
ms.assetid: 094917ac-99e6-489f-bc34-4249bab60f3e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::operator +=
This operator appends a string to the path.  
  
## Syntax  
  
```  
  
      CPathT< StringType >& operator +=(  
   PCXSTR pszMore   
);  
```  
  
#### Parameters  
 `pszMore`  
 The string to append.  
  
## Return Value  
 Returns the updated path.  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)