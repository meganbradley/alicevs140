---
title: "gslice_array Class"
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
ms.assetid: ad1b4514-b14a-4baf-a293-d5a8e8674c75
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# gslice_array Class
An internal, auxiliary template class that supports general slice objects by providing operations between subset arrays defined by the general slice of a valarray.  
  
## Syntax  
  
```  
template<class Type>  
   class gslice_array : public gsplice {  
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
 The class describes an object that stores a reference to an object **va** of class [valarray](../vs140/valarray-Class.md)**<Type\>**, along with an object **gs** of class [gslice](../vs140/gslice-Class.md) which describes the sequence of elements to select from the **valarray<Type\>** object.  
  
 You construct a **gslice_array<Type\>** object only by writing an expression of the form [va&#91;gs&#93;](../vs140/valarray-Class.md#valarray__operator_at). The member functions of class gslice_array then behave like the corresponding function signatures defined for **valarray<Type\>**, except that only the sequence of selected elements is affected.  
  
 The template class is created indirectly by certain valarray operations and cannot be used directly in the program. An internal auxiliary template class instead is used by the slice subscript operator:  
  
 `gslice_array`< **Type**> `valarray`< **Type**>:: `operator[]` ( **constgslice&**).  
  
 You construct a **gslice_array<Type\>** object only by writing an expression of the form **va[gsl]**, for a slice **gsl** of valarray **va**. The member functions of class gslice_array then behave like the corresponding function signatures defined for **valarray<Type\>**, except that only the sequence of selected elements is affected. The sequence controlled by the gslice_array is defined by the three parameters of the slice constructor, the index of the first element in the first slice, the number of elements in each slice, and the distance between the elements in each slice.  
  
 In the following example:  
  
```  
const size_t lv[] = {2, 3};  
const size_t dv[] = {7, 2};  
const valarray<size_t> len(lv, 2), str(dv, 2);  
// va[gslice(3, len, str)] selects elements with  
//   indices 3, 5, 7, 10, 12, 14  
```  
  
 The indices must be valid for the procedure to be valid.  
  
## Example  
 See the example for [gslice::gslice](../vs140/gslice-Class.md#gslice__gslice) for an example of how to declare and use a slice_array.  
  
## Requirements  
 **Header:** <valarray\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)