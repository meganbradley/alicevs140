---
title: "CompareStringOrdinal Method"
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
ms.assetid: ffa997fd-8cd7-40a5-b9e7-f55d40b072f4
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CompareStringOrdinal Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```cpp  
  
inline INT32 CompareStringOrdinal(  
   HSTRING lhs,   
   HSTRING rhs)  
```  
  
#### Parameters  
 `lhs`  
 The first HSTRING to compare.  
  
 `rhs`  
 The second HSTRING to compare.  
  
## Return Value  
  
|Value|Condition|  
|-----------|---------------|  
|-1|`lhs` is less than `rhs`.|  
|0|`lhs` equals `rhs`.|  
|1|`lhs` is greater than `rhs`.|  
  
## Remarks  
 Compares two specified HSTRING objects and returns an integer that indicates their relative position in a sort order.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::Details  
  
## See Also  
 [Microsoft::WRL::Wrappers::Details Namespace](../vs140/Microsoft--WRL--Wrappers--Details-Namespace.md)