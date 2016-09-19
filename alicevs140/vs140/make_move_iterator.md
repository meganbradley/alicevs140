---
title: "make_move_iterator"
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
ms.assetid: b17d1c7a-1254-4c05-a160-beb0ba461d5e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# make_move_iterator
Creates a `move iterator` that contains the provided iterator as the `stored` iterator.  
  
## Syntax  
  
```  
template<class Iterator>  
    move_iterator<Iterator> make_move_iterator(  
        const Iterator& _It  
);  
```  
  
#### Parameters  
 `_It`  
 The iterator stored in the new move iterator.  
  
## Remarks  
 The template function returns `move_iterator``<Iterator>(``_It``)`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [<iterator\>](../vs140/-iterator-.md)   
 [advance](../vs140/advance--STL-Samples-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)