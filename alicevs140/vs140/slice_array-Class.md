---
title: "slice_array Class"
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
ms.assetid: a182d5f7-f35c-4e76-86f2-b5ac64ddc846
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# slice_array Class
An internal, auxiliary template class that supports slice objects by providing operations between subset arrays defined by the slice of a valarray.  
  
## Syntax  
  
```  
template<class Type>  
   class slice_array : public slice {  
public:  
   typedef Type value_type;  
   void operator=(  
      const valarray<Type>& x  
   ) const;  
   void operator=(  
      const Type& x  
   ) const;  
   void operator*=(  
      const valarray<Type>& x  
   ) const;  
   void operator/=(  
      const valarray<Type>& x  
   ) const;  
   void operator%=(  
      const valarray<Type>& x  
   ) const;  
   void operator+=(  
      const valarray<Type>& x  
   ) const;  
   void operator-=(  
      const valarray<Type>& x  
   ) const;  
   void operator^=(  
      const valarray<Type>& x  
   ) const;  
   void operator&=(  
      const valarray<Type>& x  
   ) const;  
   void operator|=(  
      const valarray<Type>& x  
   ) const;  
   void operator<<=(  
      const valarray<Type>& x  
   ) const;  
   void operator>>=(  
      const valarray<Type>& x  
   ) const;  
// The rest is private or implementation defined  
}  
```  
  
## Remarks  
 The class describes an object that stores a reference to an object of class [valarray](../vs140/valarray-Class.md)**<Type\>**, along with an object of class [slice](../vs140/slice-Class.md), which describes the sequence of elements to select from the **valarray<Type\>** object.  
  
 The template class is created indirectly by certain valarray operations and cannot be used directly in the program. An internal, auxiliary template class that is used by the slice subscript operator:  
  
 `slice_array`< **Type**> `valarray`< **Type**:: `operator[]` ( `slice`).  
  
 You construct a **slice_array<Type\>** object only by writing an expression of the form [va&#91;sl&#93;](../vs140/valarray-Class.md#valarray__operator_at), for a slice **sl** of valarray **va**. The member functions of class slice_array then behave like the corresponding function signatures defined for **valarray<Type\>**, except that only the sequence of selected elements is affected. The sequence controlled by the slice_array is defined by the three parameters of the slice constructor, the index of the first element in the slice, the number of elements, and the distance between the elements. A slice_array cut from valarray **va** declared by **va**[ `slice`(2, 5, 3)] selects elements with indices 2, 5, 8, 11, and 14 from **va**. The indices must be valid for the procedure to be valid.  
  
## Example  
 See the example for [slice::slice](../vs140/slice-Class.md#slice__slice) for an example of how to declare and use a slice_array.  
  
## Requirements  
 **Header:** <valarray\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)