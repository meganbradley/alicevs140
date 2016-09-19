---
title: "reverse_iterator::reference"
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
ms.assetid: 6ad778be-e405-4e00-bcc3-df01cd982e58
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reverse_iterator::reference
A type that provides a reference to an element addressed by a reverse_iterator.  
  
## Syntax  
  
```  
typedef typename iterator_traits<RandomIterator>::reference reference;  
```  
  
## Remarks  
 The type is a synonym for the iterator trait typename `iterator_traits`<*RandomIterator*>**::reference**.  
  
## Example  
 See [reverse_iterator::operator&#91;&#93;](../vs140/reverse_iterator--operator.md) or [reverse_iterator::operator*](../vs140/reverse_iterator--operator-.md) for examples of how to declare and use **reference**.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [reverse_iterator Class](../vs140/reverse_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)