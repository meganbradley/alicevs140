---
title: "vector::capacity (STL-CLR)"
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
H1: vector::capacity (STL/CLR)
ms.assetid: f82d8da9-8b4d-4288-8d18-8e9ca5911d87
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::capacity (STL-CLR)
Reports the size of allocated storage for the container.  
  
## Syntax  
  
```  
size_type capacity();  
```  
  
## Remarks  
 The member function returns the storage currently allocated to hold the controlled sequence, a value at least as large as [size](../vs140/vector--size--STL-CLR-.md)`()`. You use it to determine how much the container can grow before it must reallocate storage for the controlled sequence.  
  
## Example  
  
```  
// cliext_vector_capacity.cpp   
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
 [reserve](../vs140/vector--reserve--STL-CLR-.md)