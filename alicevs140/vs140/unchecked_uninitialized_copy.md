---
title: "unchecked_uninitialized_copy"
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
ms.assetid: 38568841-314e-446b-91d0-92cc231e3b3c
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# unchecked_uninitialized_copy
Same as [uninitialized_copy](../vs140/uninitialized_copy.md) but allows the use of an unchecked iterator as output iterator when _SECURE_SCL=1 is defined. This function is defined in the [stdext](../vs140/stdext-Namespace.md) namespace.  
  
> [!NOTE]
>  This algorithm is a Microsoft extension to the Standard C++ Library. Code implemented using this algorithm will not be portable.  
  
## Syntax  
  
```  
template<class InputIterator, class ForwardIterator>  
   ForwardIterator unchecked_uninitialized_copy(  
      InputIterator _First,  
      InputIterator _Last,  
      ForwardIterator _Dest  
   );  
  
template<class InputIterator, class ForwardIterator, class Allocator>  
   ForwardIterator unchecked_uninitialized_copy(  
      InputIterator _First,  
      InputIterator _Last,  
      ForwardIterator _Dest,  
      Allocator& _Al  
   );  
```  
  
#### Parameters  
 `_First`  
 An input iterator addressing the first element in the source range to be copied.  
  
 `_Last`  
 An input iterator addressing the last element in the source range to be copied.  
  
 `_Dest`  
 A forward iterator addressing the first element in the destination range to be copied.  
  
 `_Al`  
 The allocator class to use with this object. [vector::get_allocator](../vs140/vector--get_allocator.md) returns the allocator class for the object.  
  
## Return Value  
 A forward iterator addressing the position one past the final element in the destination range that is receiving the copy.  
  
## Remarks  
 See [uninitialized_copy](../vs140/uninitialized_copy.md) for a code sample.  
  
 For more information on checked iterators, see [Checked Iterators](../vs140/Checked-Iterators.md).  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** stdext