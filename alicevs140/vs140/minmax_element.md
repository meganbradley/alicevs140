---
title: "minmax_element"
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
ms.assetid: a86609c2-5f54-4746-b3fb-601038062b09
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# minmax_element
Performs the work performed by `min_element` and `max_element` in one call.  
  
## Syntax  
  
```  
template<class ForwardIterator>  
    pair< ForwardIterator, ForwardIterator >  
        minmax_element(  
            ForwardIterator _First,   
            ForwardIterator _Last  
 );  
template<class ForwardIterator, class BinaryPredicate>  
    pair< ForwardIterator, ForwardIterator >  
        minmax_element(  
            ForwardIterator _First,   
            ForwardIterator _Last,   
            BinaryPredicate _Comp  
);  
```  
  
#### Parameters  
 `_First`  
 A forward iterator that indicates the beginning of a range.  
  
 `_Last`  
 A forward iterator that indicates the end of a range.  
  
 `_Comp`  
 An optional test used to order elements.  
  
## Return Value  
 Returns  
  
 `pair<ForwardIterator, ForwardIterator>`  
  
 `(` [min_element](../vs140/min_element.md)(`_First`, `_Last`), [max_element](../vs140/max_element.md)(`_First`, `_Last`)).  
  
## Remarks  
 The first template function returns  
  
 `pair<ForwardIterator,ForwardIterator>`  
  
 `(min_element(_First, _Last),max_element(_First, _Last))`.  
  
 The second template function behaves the same, except that it replaces `operator<(X, Y)` with `_Comp``(X, Y)`.  
  
 If the sequence is non-empty, the function performs at most `3 * (``_Last` `-` `_First` `- 1) / 2` comparisons.  
  
## Requirements  
 **Header:** <algorithm\>  
  
 **Namespace:** std  
  
## See Also  
 [minmax_element](../vs140/minmax_element.md)   
 [min](../vs140/min.md)   
 [min_element](../vs140/min_element.md)   
 [max](../vs140/max.md)   
 [max_element](../vs140/max_element.md)   
 [<algorithm\>](../vs140/-algorithm-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)