---
title: "copy_async Function (Concurrency::graphics Namespace)"
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
ms.assetid: 76cedd5a-bf84-40bd-b0b5-57026a261aad
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# copy_async Function (Concurrency::graphics Namespace)
Asynchronously copies a source texture into a destination buffer, or copies a source buffer into a destination buffer, and then returns a [completion_future](../vs140/completion_future-Class.md) object that can be waited on. Data can't be copied when code is running on an accelerator. The general form of this function is `copy(src, dest)`.  
  
## Syntax  
  
```  
template<  
   typename _Src_type,  
   typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   const _Src_type &_Src,  
   _Out_ void * _Dst,  
   unsigned int _Dst_byte_size  
);  
  
template<  
   typename _Src_type,  
   typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   const _Src_type &_Src,  
   const index<_Src_type::rank> &_Src_offset,  
   const extent<_Src_type::rank> &_Copy_extent,  
   _Out_ void * _Dst,  
   unsigned int _Dst_byte_size  
);  
  
template <  
   typename _Dst_type,  
   typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   const void * _Src,  
   unsigned int _Src_byte_size,  
   _Dst_type & _Dst  
);  
  
template <  
   typename _Dst_type,  
   typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   const void * _Src,  
   unsigned int _Src_byte_size,  
   _Dst_type & _Dst,  
   const index<_Dst_type::rank> &_Dst_offset,  
   const extent<_Dst_type::rank> &_Copy_extent  
);  
  
template <  
   typename InputIterator,  
   typename _Dst_type,  
   typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   InputIterator _First,  
   InputIterator _Last,  
   _Dst_type &_Dst  
);  
  
template <  
   typename InputIterator,  
   typename _Dst_type,  
   typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   InputIterator _First,  
   InputIterator _Last,  
   _Dst_type &_Dst,  
   const index<_Dst_type::rank> &_Dst_offset,  
   const extent<_Dst_type::rank> &_Copy_extent  
);  
  
template <  
   typename _Src_type,  
   typename OutputIterator,  
   typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture && !details::texture_traits<OutputIterator>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   _Src_type &_Src,  
   OutputIterator _Dst  
);  
  
template <  
   typename _Src_type,  
   typename OutputIterator,  
   typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture && !details::texture_traits<OutputIterator>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   _Src_type &_Src,  
   const index<_Src_type::rank> &_Src_offset,  
   const extent<_Src_type::rank> &_Copy_extent,  
   OutputIterator _Dst  
);  
  
template <  
   typename _Src_type,  
   typename _Dst_type,  
   typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture && details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   _Src_type &_Src,  
   _Dst_type &_Dst  
);  
  
template <  
   typename _Src_type,  
   typename _Dst_type,  
   typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture && details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(  
   _Src_type &_Src,  
   const index<_Src_type::rank> &_Src_offset,  
   _Dst_type &_Dst,  
   const index<_Dst_type::rank> &_Dst_offset,  
   const extent<_Src_type::rank> &_Copy_extent  
);  
```  
  
#### Parameters  
 `_Copy_extent`  
 The extent of the texture section to be copied.  
  
 `_Dst`  
 The object to copy to.  
  
 `_Dst_byte_size`  
 The number of bytes in the destination.  
  
 `_Dst_type`  
 The type of the destination object.  
  
 `_Dst_offset`  
 The offset into the destination at which to begin copying.  
  
 `InputIterator`  
 The type of the input interator.  
  
 `OutputIterator`  
 The type of the output iterator.  
  
 `_Src`  
 To object to copy.  
  
 `_Src_byte_size`  
 The number of bytes in the source.  
  
 `_Src_type`  
 The type of the source object.  
  
 `_Src_offset`  
 The offset into the source from which to begin copying.  
  
 `_First`  
 A beginning iterator into the source container.  
  
 `_Last`  
 An ending iterator into the source container.  
  
## Remarks  
 The copy operation always performs a deep copy.  
  
 If the extents of the source and destination objects do not match, a [runtime_exception](../vs140/runtime_exception-Class.md) is thrown.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)