---
title: "bidirectional_iterator_tag Struct"
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
ms.assetid: 9ac06066-b8ae-44b6-bee4-b05855f6a31a
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bidirectional_iterator_tag Struct
A class that provides a return type for **iterator_category** function that represents a bidirectional iterator.  
  
## Syntax  
  
```  
struct bidirectional_iterator_tag    : public forward_iterator_tag {};  
  
```  
  
## Remarks  
 The category tag classes are used as compile tags for algorithm selection. The template function needs to find the most specific category of its iterator argument, so that it can use the most efficient algorithm at compile time. For every iterator of type `Iterator`, `iterator_traits`< `Iterator`>:: **iterator_category** must be defined to be the most specific category tag that describes the iterator's behavior.  
  
 The type is the same as **iterator**< **Iter**>:: **iterator_category** when **Iter** describes an object that can serve as a bidirectional iterator.  
  
## Example  
 See [random_access_iterator_tag](../vs140/random_access_iterator_tag-Struct.md) for an example of how to use `bidirectional_iterator_tag`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [forward_iterator_tag Class](../vs140/forward_iterator_tag-Struct.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)