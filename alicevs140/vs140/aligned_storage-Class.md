---
title: "aligned_storage Class"
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
ms.assetid: f255e345-1f05-4d07-81e4-017f420839fb
caps.latest.revision: 21
translation.priority.mt: 
  - de-de
  - ja-jp
---
# aligned_storage Class
Makes suitably aligned type.  
  
## Syntax  
  
```  
template<std::size_t Len, std::size_t Align>  
    struct aligned_storage;  
  
template <std::size_t Len, std::size_t Align = alignment_of<max_align_t>::value>  
    using aligned_storage_t = typename aligned_storage<Len, Align>::type;  
```  
  
#### Parameters  
 `Len`  
 The object size.  
  
 `Align`  
 The object alignment.  
  
## Remarks  
 The template member typedef `type` is a synonym for a POD type with alignment `Align` and size `Len`. `Align` must be equal to `alignment_of<T>::value` for some type `T`, or to the default alignment.  
  
## Example  
  
```  
#include <type_traits>   
#include <iostream>   
  
typedef std::aligned_storage<sizeof (int),   
    std::alignment_of<double>::value>::type New_type;   
int main()   
    {   
    std::cout << "alignment_of<int> == "   
        << std::alignment_of<int>::value << std::endl;   
    std::cout << "aligned to double == "   
        << std::alignment_of<New_type>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **alignment_of<int\> == 4**  
**aligned to double == 8**    
## Requirements  
 **Header:** <type_traits>  
  
 **Namespace:** std  
  
## See Also  
 [<type_traits>](../vs140/-type_traits-.md)   
 [alignment_of](../vs140/alignment_of-Class.md)