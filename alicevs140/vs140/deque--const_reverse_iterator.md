---
title: "deque::const_reverse_iterator"
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
ms.assetid: c44561a2-0845-4316-80d2-a8cc99dde835
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::const_reverse_iterator
A type that provides a random-access iterator that can read any **const** element in the deque.  
  
## Syntax  
  
```  
typedef std::reverse_iterator<const_iterator> const_reverse_iterator;  
```  
  
## Remarks  
 A type `const_reverse_iterator` cannot modify the value of an element and is used to iterate through the deque in reverse.  
  
## Example  
 See the example for [rbegin](../vs140/deque--rbegin.md) for an example of how to declare and use an iterator.  
  
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)