---
title: "copy Function"
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
ms.assetid: cf3cda4b-5c64-4083-a0aa-39de2b378802
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# copy Function
Copies a C++ AMP object. All synchronous data transfer requirements are met. You can't copy data when running code on an accelerator. The general form of this function is `copy(src, dest)`.  
  
## Syntax  
  
```  
template <  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array<_Value_type, _Rank>& _Src,  
   array<_Value_type, _Rank>& _Dest  
);  
  
template <  
   typename InputIterator,  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   InputIterator _SrcFirst,  
   InputIterator _SrcLast,  
   array<_Value_type, _Rank> &_Dest  
);  
  
template <  
   typename InputIterator,  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   InputIterator _SrcFirst,  
   array<_Value_type, _Rank> &_Dest  
);  
  
template <  
   typename OutputIterator,  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array<_Value_type, _Rank> &_Src,  
   OutputIterator _DestIter  
);  
  
template <  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array<_Value_type, _Rank>& _Src,  
   array_view<_Value_type, _Rank>& _Dest  
);  
  
template <  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array_view<const _Value_type, _Rank>& _Src,  
   array<_Value_type, _Rank>& _Dest  
);  
  
template <  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array_view<_Value_type, _Rank>& _Src,  
   array<_Value_type, _Rank>& _Dest  
);  
  
template <  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array_view<const _Value_type, _Rank>& _Src,  
   array_view<_Value_type, _Rank>& _Dest  
);  
  
template <  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array_view<_Value_type, _Rank>& _Src,  
   array_view<_Value_type, _Rank>& _Dest  
);  
  
template <  
   typename InputIterator,  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   InputIterator _SrcFirst,  
   InputIterator _SrcLast,  
   array_view<_Value_type, _Rank> &_Dest  
);  
  
template <  
   typename InputIterator,  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   InputIterator _SrcFirst,  
   array_view<_Value_type, _Rank> &_Dest  
);  
  
template <  
   typename OutputIterator,  
   typename _Value_type,  
   int _Rank  
>  
void copy(  
   const array_view<_Value_type, _Rank> &_Src,  
   OutputIterator _DestIter  
);  
```  
  
#### Parameters  
 `_Dest`  
 The object to copy to.  
  
 `_DestIter`  
 An output iterator to the beginning position at destination.  
  
 `InputIterator`  
 The type of the input interator.  
  
 `OutputIterator`  
 The type of the output iterator.  
  
 `_Rank`  
 The rank of the object to copy from or the object to copy to.  
  
 `_Src`  
 To object to copy.  
  
 `_SrcFirst`  
 A beginning iterator into the source container.  
  
 `_SrcLast`  
 An ending iterator into the source container.  
  
 `_Value_type`  
 The data type of the elements that are copied.  
  
## Remarks  
 The copy operation always performs a deep copy.  
  
 If the extents of the source and destination objects do not match, a [runtime_exception](../vs140/runtime_exception-Class.md) is thrown.  
  
 You can copy to [array](../vs140/array-Class.md) and [array_view](../vs140/array_view-Class.md) objects from the following sources:  
  
-   An `array` or `array_view` that has the same rank and element type as the destination `array` or `array_view`.  
  
-   A standard container whose element type is the same as the destination `array` or `array_view`. Containers that expose `size()` and `data()` members perform more efficiently.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)