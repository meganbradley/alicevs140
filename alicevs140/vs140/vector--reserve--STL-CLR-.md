---
title: "vector::reserve (STL-CLR)"
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
H1: vector::reserve (STL/CLR)
ms.assetid: d1d5ede9-9628-4b55-95ec-f087a57205f2
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::reserve (STL-CLR)
Ensures a minimum growth capacity for the container.  
  
## Syntax  
  
```  
void reserve(size_type count);  
```  
  
#### Parameters  
 count  
 New minimum capacity of the container.  
  
## Remarks  
 The member function ensures that `capacity()` henceforth returns at least `count`. You use it to ensure that the container need not reallocate storage for the controlled sequence until it has grown to the specified size.  
  
## Example  
  
```  
// cliext_vector_reserve.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for (int i = 0; i < c1.size(); ++i)   
        System::Console::Write(" {0}", c1.at(i));   
    System::Console::WriteLine();   
  
// increase capacity   
    cliext::vector<wchar_t>::size_type cap = c1.capacity();   
    System::Console::WriteLine("capacity() = {0}, ok = {1}",   
        cap, c1.size() <= cap);   
    c1.reserve(cap + 5);   
    System::Console::WriteLine("capacity() = {0}, ok = {1}",   
        c1.capacity(), cap + 5 <= c1.capacity());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**capacity() = 4, ok = True**  
**capacity() = 9, ok = True**   
## Description  
 Note that the actual capacities may differ from the values shown here, so long as all `ok` tests report true.  
  
## Requirements  
 **Header:** <cliext/vector>  
  
 **Namespace:** cliext  
  
## See Also  
 [vector](../Topic/vector%20\(STL-CLR\).md)   
 [capacity](../vs140/vector--capacity--STL-CLR-.md)   
 [resize](../vs140/vector--resize--STL-CLR-.md)