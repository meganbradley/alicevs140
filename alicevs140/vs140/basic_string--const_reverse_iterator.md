---
title: "basic_string::const_reverse_iterator"
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
ms.assetid: 8dfaa2cf-0e0f-42c0-a214-67db377ab062
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_string::const_reverse_iterator
A type that provides a random-access iterator that can read any **const** element in the string.  
  
## Syntax  
  
```  
typedef std::reverse_iterator<const_iterator> const_reverse_iterator;  
```  
  
## Remarks  
 A type `const_reverse_iterator` cannot modify the value of a character and is used to iterate through a string in reverse.  
  
## Example  
 See the example for [rbegin](../vs140/basic_string--rbegin.md) for an example of how to declare and use `const_reverse_iterator`.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_string Class](../vs140/basic_string-Class.md)