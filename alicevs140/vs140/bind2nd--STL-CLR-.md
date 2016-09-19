---
title: "bind2nd (STL-CLR)"
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
ms.topic: reference
H1: bind2nd (STL/CLR)
ms.assetid: 457cebea-38e4-4466-a468-fe9eb138e80c
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bind2nd (STL-CLR)
Generates a `binder2nd` for an argument and functor.  
  
## Syntax  
  
```  
template<typename Fun,  
    typename Arg>  
    binder2nd<Fun> bind2nd(Fun% functor,  
        Arg right);  
```  
  
## Template Parameters  
 Arg  
 The type of the argument.  
  
 Fun  
 The type of the functor.  
  
## Function Parameters  
 functor  
 The functor to wrap.  
  
 right  
 The second argument to wrap.  
  
## Remarks  
 The template function returns [binder2nd](../vs140/binder2nd--STL-CLR-.md)`<Fun>(functor, right)`. You use it as a convenient way to wrap a two-argument functor and its second argument in a one-argument functor that calls it with a first argument.  
  
## Example  
  
```  
// cliext_bind2nd.cpp   
// compile with: /clr   
#include <cliext/algorithm>   
#include <cliext/functional>   
#include <cliext/vector>   
  
typedef cliext::vector<int> Myvector;   
int main()   
    {   
    Myvector c1;   
    c1.push_back(4);   
    c1.push_back(3);   
    Myvector c3(2, 0);   
  
// display initial contents " 4 3"   
    for each (int elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// transform and display   
    cliext::minus<int> sub_op;   
    cliext::binder2nd<cliext::minus<int> > sub4(sub_op, 4);   
  
    cliext::transform(c1.begin(), c1.begin() + 2, c3.begin(),   
        sub4);   
    for each (int elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// transform and display with function   
    cliext::transform(c1.begin(), c1.begin() + 2, c3.begin(),   
        bind2nd(sub_op, 4));   
    for each (int elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **4 3**  
 **0 -1**  
 **0 -1**   
## Requirements  
 **Header:** <cliext/functional>  
  
 **Namespace:** cliext  
  
## See Also  
 [binder2nd](../vs140/binder2nd--STL-CLR-.md)