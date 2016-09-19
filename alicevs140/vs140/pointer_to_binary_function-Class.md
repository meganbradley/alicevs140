---
title: "pointer_to_binary_function Class"
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
ms.assetid: fb50599f-bcb3-4076-a669-6dcc3eb189a5
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pointer_to_binary_function Class
Converts a binary function pointer into an adaptable binary function.  
  
## Syntax  
  
```  
template<class Arg1, class Arg2, class Result>  
   class pointer_to_binary_function   
   : public binary_function <Arg1, Arg2, Result>   
   {  
   public:  
   explicit pointer_to_binary_function(  
      Result (* _pfunc )( Arg1, Arg2 )   
   );  
   Result operator()(  
      Arg1 _Left,   
      Arg2 _Right  
   ) const;  
   };  
```  
  
#### Parameters  
 `_pfunc`  
 The binary function to be converted.  
  
 `_Left`  
 The left object that the                         *\*_pfunc* is called on.  
  
 `_Right`  
 The right object that the                         *\*_pfunc* is called on.  
  
## Return Value  
 The template class stores a copy of **_pfunc**. It defines its member function `operator()` as returning (\* **_pfunc**)(_                *Left*, \_                *Right*).  
  
## Remarks  
 A binary function pointer is a function object and may be passed to any Standard Template Library algorithm that is expecting a binary function as a parameter, but it is not adaptable. To use it with an adaptor, such as binding a value to it or using it with a negator, it must be supplied with the nested types **first_argument_type**, **second_argument_type**, and **result_type** that make such an adaptation possible. The conversion by `pointer_to_binary_function` allows the function adaptors to work with binary function pointers.  
  
## Example  
 The constructor of `pointer_to_binary_function` is rarely used directly. See the helper function [ptr_fun](../vs140/-functional--functions.md#ptr_fun_function) for an example of how to declare and use the `pointer_to_binary_function` adaptor predicate.  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)