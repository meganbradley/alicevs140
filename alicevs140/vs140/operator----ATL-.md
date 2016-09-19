---
title: "operator &lt; (ATL)"
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
ms.assetid: 895f64fa-5792-4b86-a2a4-c8180de18e70
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator &lt; (ATL)
Tests if the `CSid` object or `SID` structure on the left side of the operator is less than the `CSid` object or `SID` structure on the right side (for STL compatibility).  
  
## Syntax  
  
```  
  
      bool operator <(  
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
 Returns **true** if the address of the `lhs` object is less than the address of the `rhs` object, **false** otherwise.  
  
## Remarks  
 This operator acts on the address of the `CSid` object or `SID` structure, and is implemented to provide compatibility with STL collection classes.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [Operators Alphabetical Reference](../vs140/ATL-Operators-Alphabetical-Reference.md)   
 [operator >](../vs140/operator----ATL-.md)