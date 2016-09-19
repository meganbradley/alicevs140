---
title: "add_cv Class"
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
ms.assetid: a5572c78-a097-45d7-b476-ed4876889dea
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# add_cv Class
Makes const/volatile type from type.  
  
## Syntax  
  
```  
template<class Ty>  
    struct add_cv;  
  
template<class T>using add_cv_t = typename add_cv<T>::type;  
```  
  
#### Parameters  
 `Ty`  
 The type to modify.  
  
## Remarks  
 An instance of the type modifier holds the modified-type [add_volatile](../vs140/add_volatile-Class.md)`<` [add_const](../vs140/add_const-Class.md)`<Ty> >`.  
  
## Example  
  
```  
#include <type_traits>   
#include <iostream>   
  
int main()   
    {   
    std::add_cv_t<int> *p = (const volatile int *)0;   
  
    p = p;  // to quiet "unused" warning   
    std::cout << "add_cv<int> == "   
        << typeid(*p).name() << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **add_cv_t<int\> == int**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [remove_const](../vs140/remove_const-Class.md)   
 [remove_volatile](../vs140/remove_volatile-Class.md)