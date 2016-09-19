---
title: "remove_const Class"
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
ms.assetid: feb76fb3-9228-41d6-80f6-2fbb04daec43
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# remove_const Class
Makes a non const type from type.  
  
## Syntax  
  
```  
template<class T>  
    struct remove_const;  
```  
  
```  
template<class T>  
  using remove_const_t = typename remove_const<T>::type;  
```  
  
#### Parameters  
 `T`  
 The type to modify.  
  
## Remarks  
 An instance of `remove_const<T>` holds a modified-type that is `T1` when `T` is of the form `const T1`, otherwise `T`.  
  
## Example  
  
```  
#include <type_traits>   
#include <iostream>   
  
int main()   
    {   
    int *p = (std::remove_const_t<const int>*)0;   
  
    p = p;  // to quiet "unused" warning   
    std::cout << "remove_const_t<const int> == "   
        << typeid(*p).name() << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **remove_const_t<const int\> == int**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [add_const](../vs140/add_const-Class.md)   
 [remove_cv](../vs140/remove_cv-Class.md)