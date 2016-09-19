---
title: "move_iterator::move_iterator"
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
ms.assetid: 926b98d9-7aa4-450f-adc2-9adeb6b3930c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# move_iterator::move_iterator
Constructs a move iterator. Uses the parameter as the stored iterator.  
  
## Syntax  
  
```  
move_iterator();  
explicit move_iterator(RandomIterator _Right);  
template<class Type>  
    move_iterator(const move_iterator<Type>& _Right);  
```  
  
#### Parameters  
 `_Right`  
 The iterator to use as the stored iterator.  
  
## Remarks  
 The first constructor initializes the stored iterator with its default constructor. The remaining constructors initialize the stored iterator with `base.base()`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [move_iterator Class](../vs140/move_iterator-Class.md)   
 [<iterator\>](../vs140/-iterator-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)