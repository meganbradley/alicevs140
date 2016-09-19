---
title: "add_volatile Class"
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
ms.assetid: cde57277-d764-402d-841e-97611ebaab14
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# add_volatile Class
Makes volatile type from the specified type.  
  
## Syntax  
  
```  
template<class Ty>  
    struct add_volatile;  
  
template<class T>using add_volatile_t = typename add_volatile<T>::type;  
```  
  
#### Parameters  
 `Ty`  
 The type to modify.  
  
## Remarks  
 An instance of the type modifier holds a modified-type that is `Ty` if `Ty` is a reference, a function, or a volatile-qualified type, otherwise `volatile Ty`.  
  
## Example  
  
```  
#include <type_traits>   
#include <iostream>   
  
int main()   
    {   
    std::add_volatile_t<int> *p = (volatile int *)0;   
  
    p = p;  // to quiet "unused" warning   
    std::cout << "add_volatile<int> == "   
        << typeid(*p).name() << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **add_volatile<int\> == int**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [remove_volatile](../vs140/remove_volatile-Class.md)