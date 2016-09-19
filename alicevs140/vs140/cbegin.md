---
title: "cbegin"
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
ms.assetid: 9ffd573c-6c7d-4798-9873-ea2f977dcf79
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cbegin
Retrieves a const iterator to the first element in a specified container.  
  
## Syntax  
  
```cpp  
template<class Container>  
    auto cbegin(const Container& cont)   
        -> decltype(cont.begin());  
  
```  
  
#### Parameters  
 `cont`  
 A container or initializer_list.  
  
## Return Value  
 A constant `cont.begin()`.  
  
## Remarks  
 This function works with all STL containers and with [initializer_list](../vs140/initializer_list-Class.md).  
  
 You can use this member function in place of the `begin()` template function to guarantee that the return value is `const_iterator`. Typically, it's used in conjunction with the [auto](../vs140/auto--C---.md) type deduction keyword, as shown in the following example. In the example, consider `Container` to be a modifiable (non-`const`) container or `initializer_list` of any kind that supports `begin()` and `cbegin()`.  
  
```cpp  
  
auto i1 = Container.begin();  // i1 is Container<T>::iterator  
auto i2 = Container.cbegin(); // i2 is Container<T>::const_iterator  
```  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [<iterator\>](../vs140/-iterator-.md)   
 [begin](../vs140/begin.md)   
 [cend](../vs140/cend.md)   
 [end](../vs140/end.md)