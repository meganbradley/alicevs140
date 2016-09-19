---
title: "HString::Operator!= Operator"
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
ms.assetid: dcdd2aca-e7d6-4bf1-b2de-03efbb430a93
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HString::Operator!= Operator
Indicates whether the two parameters are not equal.  
  
## Syntax  
  
```cpp  
  
   inline bool operator!=(  
                  const HString& lhs,   
                  const HString& rhs) throw()  
  
inline bool operator!=(  
                  const HStringReference& lhs,   
                  const HString& rhs) throw()  
  
inline bool operator!=(  
                  const HString& lhs,   
                  const HStringReference& rhs) throw()  
  
inline bool operator!=(  
                  const HSTRING& lhs,   
                  const HString& rhs) throw()  
  
inline bool operator!=(  
                  const HString& lhs,   
                  const HSTRING& rhs) throw()  
  
```  
  
#### Parameters  
 `lhs`  
 The first parameter to compare. `lhs` can be an HString or HStringReference object, or an HSTRING handle.  
  
 `rhs`  
 The second parameter to compare.`rhs` can be an HString or HStringReference object, or an HSTRING handle.  
  
## Return Value  
 `true` if the `lhs` and `rhs` parameters are not equal; otherwise, `false`.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [HString Class](../vs140/HString-Class.md)