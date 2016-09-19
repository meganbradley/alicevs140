---
title: "HStringReference::Operator&lt; Operator"
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
ms.assetid: 55aa48e8-7c96-4123-9ebe-42b4cd8b9377
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HStringReference::Operator&lt; Operator
Indicates whether the first parameter is less than the second parameter.  
  
## Syntax  
  
```cpp  
  
inline bool operator<(  
    const HStringReference& lhs,   
    const HStringReference& rhs) throw()  
```  
  
#### Parameters  
 `lhs`  
 The first parameter to compare. `lhs` can be a reference to an HStringReference.  
  
 `rhs`  
 The second parameter to compare.  `rhs` can be a reference to an HStringReference.  
  
## Return Value  
 `true` if the `lhs` parameter is less than the `rhs` parameter; otherwise, `false`.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HStringReference Class](../vs140/HStringReference-Class.md)