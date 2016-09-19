---
title: "unordered_map::cend"
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
ms.assetid: a710d8f7-87ba-49d1-b64e-e6f617e525fb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unordered_map::cend
Returns a `const` iterator that addresses the location just beyond the last element in a range.  
  
## Syntax  
  
```  
const_iterator cend() const;  
```  
  
## Return Value  
 A `const` forward-access iterator that points just beyond the end of the range.  
  
## Remarks  
 `cend` is used to test whether an iterator has passed the end of its range.  
  
 You can use this member function in place of the `end()` member function to guarantee that the return value is `const_iterator`. Typically, it's used in conjunction with the [auto](../vs140/auto--C---.md) type deduction keyword, as shown in the following example. In the example, consider `Container` to be a modifiable (non-`const`) container of any kind that supports `end()` and `cend()`.  
  
```cpp  
  
auto i1 = Container.end();  // i1 is Container<T>::iterator   
auto i2 = Container.cend(); // i2 is Container<T>::const_iterator  
```  
  
 The value returned by `cend` should not be dereferenced.  
  
## Requirements  
 **Header:** <unordered_map>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_map>](../vs140/-unordered_map-.md)   
 [unordered_map Class](../vs140/unordered_map-Class.md)   
 [unordered_map::begin](../vs140/unordered_map--begin.md)