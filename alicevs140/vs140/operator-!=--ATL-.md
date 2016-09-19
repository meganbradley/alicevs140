---
title: "operator != (ATL)"
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
ms.assetid: d2a0720d-2664-479e-bd70-11704c21973f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator != (ATL)
Compares `CSid` objects or `SID` (security identifier) structures for inequality.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   const CSid & lhs,   
   const CSid & rhs,   
) throw();  
```  
  
#### Parameters  
 `lhs`  
 The first `CSid` object or `SID` structure to compare.  
  
 `rhs`  
 The second `CSid` object or `SID` structure to compare.  
  
## Return Value  
 Returns **true** if the objects are not equal, **false** if they are equal.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [Operators Alphabetical Reference](../vs140/ATL-Operators-Alphabetical-Reference.md)   
 [operator ==](../vs140/operator-==--ATL-.md)