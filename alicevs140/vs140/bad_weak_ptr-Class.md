---
title: "bad_weak_ptr Class"
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
ms.assetid: a09336d5-7237-4480-ab6b-3787e0e6025e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bad_weak_ptr Class
Reports bad weak_ptr exception.  
  
## Syntax  
  
```  
class bad_weak_ptr  
    : public std::exception {  
public:  
    bad_weak_ptr();  
    const char *what() throw();  
    };  
```  
  
## Remarks  
 The class describes an exception that can be thrown from the [shared_ptr](../vs140/shared_ptr-Class.md) constructor that takes an argument of type [weak_ptr](../vs140/weak_ptr-Class.md). The member function `what` returns `"bad_weak_ptr"`.  
  
## Example  
  
```  
// std_tr1__memory__bad_weak_ptr.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::weak_ptr<int> wp;   
  
     {   
    std::shared_ptr<int> sp(new int);   
    wp = sp;   
     }   
  
    try   
        {   
        std::shared_ptr<int> sp1(wp); // weak_ptr has expired   
        }   
    catch (const std::bad_weak_ptr&)   
        {   
        std::cout << "bad weak pointer" << std::endl;   
        }   
    catch (...)   
        {   
        std::cout << "unknown exception" << std::endl;   
        }   
  
    return (0);   
    }  
  
```  
  
  **bad weak pointer**    
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [weak_ptr](../vs140/weak_ptr-Class.md)