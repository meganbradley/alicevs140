---
title: "ptr_fun Function"
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
ms.assetid: 1b4045ed-ef88-482f-bfe6-fb621d2f50bb
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ptr_fun Function
Helper template functions used to convert unary and binary function pointers, respectively, into unary and binary adaptable functions.  
  
## Syntax  
  
```  
  
      template<class Arg, class Result>  
   pointer_to_unary_function<Arg, Result, Result (*)(Arg)>  
      ptr_fun(Result (*_pfunc)(Arg));  
template<class Arg1, class Arg2, class Result>  
   pointer_to_binary_function<Arg1, Arg2, Result, Result (*)(Arg1, Arg2)>  
      ptr_fun(Result (*_pfunc)(Arg1, Arg2));  
```  
  
#### Parameters  
 `_pfunc`  
 The unary or binary function pointer to be converted to an adaptable function.  
  
## Return Value  
 The first template function returns the unary function [pointer_to_unary_function](../vs140/pointer_to_unary_function-Class.md) <`Arg`, **Result**>(*`_pfunc`).  
  
 The second template function returns binary function [pointer_to_binary_function](../vs140/pointer_to_binary_function-Class.md) <**Arg1**, **Arg2**, **Result**>(*`_pfunc`).  
  
## Remarks  
 A function pointer is a function object and may be passed to any Standard Template Library algorithm that is expecting a function as a parameter, but it is not adaptable. To use it with an adaptor, such as binding a value to it or using it with a negator, it must be supplied with the nested types that make such an adaptation possible. The conversion of unary and binary function pointers by the `ptr_fun` helper function allows the function adaptors to work with unary and binary function pointers.  
  
## Example  
 [!CODE [functional_ptr_fun#1](../CodeSnippet/VS_Snippets_Cpp/functional_ptr_fun#1)]  
  
## Output  
  
```  
Original sequence contains: Open up the opalescent gates  
Found a match: opalescent  
```  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [Standard Template Library](../vs140/Standard-Template-Library.md)