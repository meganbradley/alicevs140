---
title: "reverse_iterator::difference_type"
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
ms.assetid: c04277f0-a30e-4555-83b1-d927304eb0a9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# reverse_iterator::difference_type
A type that provides the difference between two `reverse_iterator`s referring to elements within the same container.  
  
## Syntax  
  
```  
  
   typedef typename iterator_traits<RandomIterator>::difference_type  
difference_type;  
```  
  
## Remarks  
 The `reverse_iterator` difference type is the same as the iterator difference type.  
  
 The type is a synonym for the iterator trait typename `iterator_traits`<**RandomIterator**>**::pointer**.  
  
## Example  
 See [reverse_iterator::operator&#91;&#93;](../vs140/reverse_iterator--operator.md) for an example of how to declare and use `difference_type`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [reverse_iterator Class](../vs140/reverse_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)