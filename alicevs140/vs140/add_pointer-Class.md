---
title: "add_pointer Class"
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
ms.assetid: d8095cb0-6578-4143-b78f-87f82485298c
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# add_pointer Class
Makes a pointer-to-type from a specified type.  
  
## Syntax  
  
```  
template<class Ty>  
    struct add_pointer;  
  
template<class T>using add_pointer_t = typename add_pointer<T>::type;  
```  
  
#### Parameters  
 `Ty`  
 The type to modify.  
  
## Remarks  
 The member typedef type names the same type as `remove_reference<T>::type*`.  
  
 Because it is invalid to make a pointer from a reference, `add_pointer` removes the reference, if any, from the specified type before it makes a pointer-to-type. Consequently, you can use a type with `add_pointer` without being concerned about whether the type is a reference.  
  
## Example  
 The following example demonstrates that `add_pointer` of a type is the same as a pointer to that type.  
  
```  
#include <type_traits>   
#include <iostream>   
  
int main()   
    {   
    std::add_pointer_t<int> *p = (int **)0;   
  
    p = p;  // to quiet "unused" warning   
    std::cout << "add_pointer_t<int> == "   
        << typeid(*p).name() << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **add_pointer_t<int\> == int \***    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [remove_pointer](../vs140/remove_pointer-Class.md)