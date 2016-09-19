---
title: "vector::assign (STL-CLR)"
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
H1: vector::assign (STL/CLR)
ms.assetid: 945e2048-6c61-4701-b13c-8241cbee3fa1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::assign (STL-CLR)
Replaces all elements.  
  
## Syntax  
  
```  
void assign(size_type count, value_type val);  
template<typename InIt>  
    void assign(InIt first, InIt last);  
void assign(System::Collections::Generic::IEnumerable<Value>^ right);  
```  
  
#### Parameters  
 count  
 Number of elements to insert.  
  
 first  
 Beginning of range to insert.  
  
 last  
 End of range to insert.  
  
 right  
 Enumeration to insert.  
  
 val  
 Value of the element to insert.  
  
## Remarks  
 The first member function replaces the controlled sequence with a repetition of `count` elements of value `val`. You use it to fill the container with elements all having the same value.  
  
 If `InIt` is an integer type, the second member function behaves the same as `assign((size_type)``first``, (value_type)``last``)`. Otherwise, it replaces the controlled sequence with the sequence `[``first``,` `last``)`. You use it to make the controlled sequence a copy another sequence.  
  
 The third member function replaces the controlled sequence with the sequence designated by the enumerator `right`. You use it to make the controlled sequence a copy of a sequence described by an enumerator.  
  
## Example  
  
```  
// cliext_vector_assign.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// assign a repetition of values   
    cliext::vector<wchar_t> c2;   
    c2.assign(6, L'x');   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign an iterator range   
    c2.assign(c1.begin(), c1.end() - 1);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign an enumeration   
    c2.assign(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c1);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **x x x x x x**  
 **a b**  
 **a b c**   
## Requirements  
 **Header:** <cliext/vector>  
  
 **Namespace:** cliext  
  
## See Also  
 [vector](../Topic/vector%20\(STL-CLR\).md)   
 [operator=](../vs140/vector--operator=--STL-CLR-.md)