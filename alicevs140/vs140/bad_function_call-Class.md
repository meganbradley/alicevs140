---
title: "bad_function_call Class"
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
ms.assetid: b70a0268-43ff-4f3b-a283-faf1cb172d4c
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bad_function_call Class
Reports a bad function call.  
  
## Syntax  
  
```  
class bad_function_call  
    : public std::exception {  
    };  
```  
  
## Remarks  
 The class describes an exception thrown to indicate that a call to `operator()` on a [function](../vs140/function-Class.md) object failed because the object was empty.  
  
## Example  
  
```  
// std_tr1__functional__bad_function_call.cpp   
// compile with: /EHsc   
#include <functional>   
#include <iostream>   
  
typedef double (Fd)(double);   
typedef std::function<Fd> Myfunc;   
  
double square(double x)   
    {   
    return (x * x);   
    }   
  
int main()   
    {   
    Myfunc fd0(square);   
    std::cout << "x * x == " << fd0(3) << std::endl;   
  
    try   
        {   
        Myfunc fd1;   
        std::cout << fd1(3) << std::endl;   
        }   
    catch (const std::bad_function_call&)   
        {   
        std::cout << "bad function call" << std::endl;   
        }   
    catch (...)   
        {   
        std::cout << "unknown exception" << std::endl;   
        }   
  
    return (0);   
    }  
  
```  
  
  **x \* x == 9**  
**bad function call**    
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std