---
title: "multimap::erase"
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
ms.assetid: f0d6cd39-759b-4478-a823-394d70219d9a
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::erase
Removes an element or a range of elements in a multimap from specified positions or removes elements that match a specified key.  
  
## Syntax  
  
```  
iterator erase(  
   const_iterator Where  
);  
iterator erase(  
   const_iterator First,  
   const_iterator Last  
);  
size_type erase(  
   const key_type& Key  
);  
```  
  
#### Parameters  
 `Where`  
 Position of the element to be removed.  
  
 `First`  
 Position of the first element to be removed.  
  
 `Last`  
 Position just beyond the last element to be removed.  
  
 `Key`  
 The key of the elements to be removed.  
  
## Return Value  
 For the first two member functions, a bidirectional iterator that designates the first element remaining beyond any elements removed, or an element that is the end of the map if no such element exists.  
  
 For the third member function, returns the number of elements that have been removed from the multimap.  
  
## Remarks  
 For a code example, see [map::erase](../vs140/map--erase.md).  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [<map\>](../vs140/-map-.md)   
 [multimap Class](../vs140/multimap-Class.md)   
 [multimap::clear](../vs140/multimap--clear.md)   
 [map::max_size, map::clear, map::erase, and map::size](../vs140/map--max_size--map--clear--map--erase--and-map--size.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)