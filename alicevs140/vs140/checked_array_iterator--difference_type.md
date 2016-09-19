---
title: "checked_array_iterator::difference_type"
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
ms.assetid: fb4ea46e-3f63-4fb6-b50e-0fa9ce555600
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# checked_array_iterator::difference_type
A type that provides the difference between two `checked_array_iterator`s referring to elements within the same container.  
  
## Syntax  
  
```  
typedef typename iterator_traits<_Iterator>::difference_type difference_type;  
```  
  
## Remarks  
 The `checked_array_iterator` difference type is the same as the iterator difference type.  
  
 See [checked_array_iterator::operator&#91;&#93;](../vs140/checked_array_iterator--operator.md) for a code sample.  
  
 For more information, see [Checked Iterators](../vs140/Checked-Iterators.md).  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [checked_array_iterator Class](../vs140/checked_array_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)