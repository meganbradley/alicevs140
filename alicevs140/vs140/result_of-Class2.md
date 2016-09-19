---
title: "result_of Class2"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: result_of Class
ms.assetid: 14ec0040-07f1-45a5-80b5-d0c9f9b00c8f
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# result_of Class2
The return type of a wrapped callable object.  
  
## Syntax  
  
```  
template<class Ty>  
    struct result_of {  
    typedef T0 type;  
    };  
```  
  
#### Parameters  
 `Ty`  
 A description of a function call (see Remarks section).  
  
## Remarks  
 The template class defines its member                 `type` as a synonym for the return type of a function call described by its template argument                 `Ty`. The template argument must be of the form                 `Fty(T1, T2, ..., TN)`, where                 `Fty` is a callable type. The template determines the return type according to the first of the following rules that applies:  
  
-   if                         `Fty` is a pointer to function type                         `R(*)(U1, U2, ..., UN)` the return type is                         `R`;  
  
-   if                         `Fty` is a reference to function type                         `R(&)(U1, U2, ..., UN)` the return type is                         `R`;  
  
-   if                         `Fty` is a pointer to member function type                         `R(U1::*)(U2, ..., UN)` the return type is                         `R`;  
  
-   if                         `Fty` is a pointer to data member type                         `R U1::*` the return type is                         `R`;  
  
-   if                         `Fty` is a class with a member typedef                         `result_type` the return type is                         `Fty::result_type`;  
  
-   if                         `N` is 0 (that is,                         `Ty` is of the form                         `Fty()`) the return type is                         `void`;  
  
-   if                         `Fty` is a class with a member template named                         `result` the return type is                         `Fty::result<T1, T2, ..., TN>::type`;  
  
-   in all other cases it is an error.  
  
## Example  
 Â  
  
```  
// std_tr1__functional__result_of.cpp   
// compile with: /EHsc   
#include <functional>   
#include <iostream>   
  
double square(double x)   
    {   
    return (x * x);   
    }   
  
template<class Fun,   
    class Arg>   
    void test_result(const Fun& fun, Arg arg)   
    {   
    typename std::result_of<Fun(Arg)>::type val = fun(arg);   
    std::cout << "val == " << val << std::endl;   
    }   
  
int main()   
    {   
    test_result(&square, 3.0);   
  
    return (0);   
    }  
  
```  
  
 **val == 9**   
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std