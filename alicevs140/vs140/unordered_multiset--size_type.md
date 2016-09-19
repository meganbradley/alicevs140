---
title: "unordered_multiset::size_type"
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
ms.assetid: 122ac436-eb52-472c-9edf-93aa03417c66
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unordered_multiset::size_type
The type of an unsigned distance between two elements.  
  
## Syntax  
  
```  
typedef T2 size_type;  
```  
  
## Remarks  
 The unsigned integer type describes an object that can represent the length of any controlled sequence. It is described here as a synonym for the implementation-defined type `T2`.  
  
## Example  
  
```  
// std_tr1__unordered_set__unordered_multiset_size_type.cpp   
// compile with: /EHsc   
#include <unordered_set>   
#include <iostream>   
  
typedef std::unordered_multiset<char> Myset;   
int main()   
    {   
    Myset c1;   
    Myset::size_type sz = c1.size();   
  
    std::cout << "size == " << sz << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **size == 0**   
## Requirements  
 **Header:** <unordered_set>  
  
 **Namespace:** std  
  
## See Also  
 [<unordered_set>](../vs140/-unordered_set-.md)   
 [unordered_multiset](../vs140/unordered_multiset-Class.md)   
 [unordered_multiset::difference_type](../vs140/unordered_multiset--difference_type.md)