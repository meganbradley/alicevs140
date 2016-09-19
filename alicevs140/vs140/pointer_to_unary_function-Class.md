---
title: "pointer_to_unary_function Class"
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
ms.assetid: 05600207-b916-4759-beca-6b6facd2d6f6
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pointer_to_unary_function Class
Converts a unary function pointer into an adaptable unary function.  
  
## Syntax  
  
```  
template<class Arg, class Result>  
class pointer_to_unary_function  
    : public unary_function<Arg, Result>   
    {  
    public:  
        explicit pointer_to_unary_function(  
            Result (* _pfunc)(Arg)  
        );  
        Result operator()(  
            Arg _Left  
        ) const;  
    };  
```  
  
#### Parameters  
 `_pfunc`  
 The binary function to be converted.  
  
 `_Left`  
 The object that the                         *\*_pfunc* is called on.  
  
## Return Value  
 The template class stores a copy of **_pfunc**. It defines its member function `operator()` as returning (\* **_pfunc**)(_                *Left*).  
  
## Remarks  
 A unary function pointer is a function object and may be passed to any Standard Template Library algorithm that is expecting a unary function as a parameter, but it is not adaptable. To use it with an adaptor, such as binding a value to it or using it with a negator, it must be supplied with the nested types **argument_type** and **result_type** that make such an adaptation possible. The conversion by `pointer_to_unary_function` allows the function adaptors to work with binary function pointers.  
  
## Example  
 The constructor of `pointer_to_unary_function` is rarely used directly. See the helper function [ptr_fun](../vs140/-functional--functions.md#ptr_fun_function) for an example of how to declare and use the `pointer_to_unary_function` adaptor predicate.  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)