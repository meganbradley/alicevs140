---
title: "remove_cv Class"
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
ms.assetid: 8502602a-1c80-479c-84e0-33bd1d6496d6
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# remove_cv Class
Makes non const/volatile type from type.  
  
## Syntax  
  
```  
template<class T>  
    struct remove_cv;  
  
template<class T>  using remove_cv_t = typename remove_cv<T>::type;  
```  
  
#### Parameters  
 `T`  
 The type to modify.  
  
## Remarks  
 An instance of `remove_cv<T>` holds a modified-type that is `T1` when `T` is of the form `const T1`, `volatile T1`, or `const volatile T1`, otherwise `T`.  
  
## Example  
  
```  
  
#include <type_traits>   
#include <iostream>   
  
int main()   
    {   
    int *p = (std::remove_cv_t<const volatile int> *)0;   
  
    p = p;  // to quiet "unused" warning   
    std::cout << "remove_cv_t<const volatile int> == "   
        << typeid(*p).name() << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **remove_cv_t<const volatile int\> == int**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [remove_const](../vs140/remove_const-Class.md)   
 [remove_volatile](../vs140/remove_volatile-Class.md)