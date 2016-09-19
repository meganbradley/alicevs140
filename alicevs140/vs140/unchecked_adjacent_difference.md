---
title: "unchecked_adjacent_difference"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a6b0b49-a84b-40b1-bcd5-3bf76c6ef7d7
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unchecked_adjacent_difference
Same as [adjacent_difference](../vs140/adjacent_difference.md), but allows the use of an unchecked iterator as output iterator when _SECURE_SCL=1 is defined.  `unchecked_adjacent_difference` is defined in the `stdext` namespace.  
  
> [!NOTE]
>  This algorithm is a Microsoft extension to the Standard C++ Library. Code implemented using this algorithm will not be portable.  
  
## Syntax  
  
```  
template<class InputIterator, class OutIterator>  
   OutputIterator unchecked_adjacent_difference(  
      InputIterator_First,  
      InputIterator _Last,  
      OutputIterator_Result   
   );  
  
template<class InputIterator, class OutputIterator, class BinaryOperation>  
   OutputIterator unchecked_adjacent_difference(  
      InputIterator_First,  
      InputIterator _Last,  
      OutputIterator_Result,   
      BinaryOperation _Binary_op  
   );  
```  
  
#### Parameters  
 `_First`  
 An input iterator addressing the first element in the input range whose elements are to be differenced with their respective predecessors or where the pair of values is to be operated on by another specified binary operation.  
  
 `_Last`  
 An input iterator addressing the last element in the input range whose elements are to be differenced with their respective predecessors or where the pair of values is to be operated on by another specified binary operation.  
  
 `_Result`  
 An output iterator addressing the first element a destination range where the series of differences or the results of the specified operation is to be stored.  
  
 `_Binary_op`  
 The binary operation that is to be applied in the generalized operation replacing the operation of subtraction in the differencing procedure.  
  
## Return Value  
 An output iterator addressing the end of the destination range: `_Result` + (`_Last` - `_First`).  
  
## Remarks  
 See [adjacent_difference](../vs140/adjacent_difference.md) for a code sample.  
  
 For more information on checked iterators, see [Checked Iterators](../vs140/Checked-Iterators.md).  
  
## Requirements  
 **Header:** <numeric\>  
  
 **Namespace:** stdext  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)