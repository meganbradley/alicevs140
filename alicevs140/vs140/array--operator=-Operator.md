---
title: "array::operator= Operator"
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
ms.topic: article
ms.assetid: a0438058-2f3c-4e03-aeab-a95b4fcdb756
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# array::operator= Operator
Copies the contents of the specified [array](../vs140/array-Class.md) object.  
  
## Syntax  
  
```  
array & operator= (  
   const array & _Other  
) restrict(cpu);  
  
array & operator= (  
   array && _Other  
) restrict(cpu);  
  
array& operator=(  
   const array_view<const _Value_type, _Rank>& _Src  
) restrict(cpu);  
```  
  
#### Parameters  
 `_Other`  
 The `array` object to copy from.  
  
 `_Src`  
 The `array` object to copy from.  
  
## Return Value  
 A reference to this `array` object.  
  
## Overloads List  
  
|Name|Description|  
|----------|-----------------|  
|||  
|`array & operator= (    const array & _Other ) restrict(cpu);`|Copies the contents of the specified [array](../vs140/array-Class.md) object into this one, using a deep copy.|  
|`array & operator= (    array && Other ) restrict(cpu);`|Copies the contents of the specified [array](../vs140/array-Class.md) object into this one, using a move assignment.|  
|`array& operator=(    const array_view<const _Value_type, _Rank>& Src ) restrict(cpu);`|Copies the `array` object into an  [array_view](../vs140/array_view-Class.md) object.|  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [array Class](../vs140/array-Class.md)