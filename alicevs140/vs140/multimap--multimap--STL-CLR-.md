---
title: "multimap::multimap (STL-CLR)"
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
H1: multimap::multimap (STL/CLR)
ms.assetid: cdf9c5dc-774c-424e-aeea-7554643e401c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::multimap (STL-CLR)
Constructs a container object.  
  
## Syntax  
  
```  
multimap();  
explicit multimap(key_compare^ pred);  
multimap(multimap<Key, Mapped>% right);  
multimap(multimap<Key, Mapped>^ right);  
template<typename InIter>  
    multimapmultimap(InIter first, InIter last);  
template<typename InIter>  
    multimap(InIter first, InIter last,  
        key_compare^ pred);  
multimap(System::Collections::Generic::IEnumerable<GValue>^ right);  
multimap(System::Collections::Generic::IEnumerable<GValue>^ right,  
    key_compare^ pred);  
```  
  
#### Parameters  
 first  
 Beginning of range to insert.  
  
 last  
 End of range to insert.  
  
 pred  
 Ordering predicate for the controlled sequence.  
  
 right  
 Object or range to insert.  
  
## Remarks  
 The constructor:  
  
 `multimap();`  
  
 initializes the controlled sequence with no elements, with the default ordering predicate `key_compare()`. You use it to specify an empty initial controlled sequence, with the default ordering predicate.  
  
 The constructor:  
  
 `explicit multimap(key_compare^ pred);`  
  
 initializes the controlled sequence with no elements, with the ordering predicate `pred`. You use it to specify an empty initial controlled sequence, with the specified ordering predicate.  
  
 The constructor:  
  
 `multimap(multimap<Key, Mapped>% right);`  
  
 initializes the controlled sequence with the sequence `[``right``.`[begin](../vs140/multimap--begin--STL-CLR-.md)`(),` `right``.`[end](../vs140/multimap--end--STL-CLR-.md)`())`, with the default ordering predicate. You use it to specify an initial controlled sequence that is a copy of the sequence controlled by the multimap object `right`, with the default ordering predicate.  
  
 The constructor:  
  
 `multimap(multimap<Key, Mapped>^ right);`  
  
 initializes the controlled sequence with the sequence `[``right``->`[begin](../vs140/multimap--begin--STL-CLR-.md)`(),` `right``->`[end](../vs140/multimap--end--STL-CLR-.md)`())`, with the default ordering predicate. You use it to specify an initial controlled sequence that is a copy of the sequence controlled by the multimap object `right`, with the default ordering predicate.  
  
 The constructor:  
  
 `template<typename InIter>`  
  
 `multimap(InIter first, InIter last);`  
  
 initializes the controlled sequence with the sequence `[``first``,` `last``)`, with the default ordering predicate. You use it to make the controlled sequence a copy of another sequence, with the default ordering predicate.  
  
 The constructor:  
  
 `template<typename InIter>`  
  
 `multimap(InIter first, InIter last,`  
  
 `key_compare^ pred);`  
  
 initializes the controlled sequence with the sequence `[``first``,` `last``)`, with the ordering predicate `pred`. You use it to make the controlled sequence a copy of another sequence, with the specified ordering predicate.  
  
 The constructor:  
  
 `multimap(System::Collections::Generic::IEnumerable<Key>^ right);`  
  
 initializes the controlled sequence with the sequence designated by the enumerator `right`, with the default ordering predicate. You use it to make the controlled sequence a copy of another sequence described by an enumerator, with the default ordering predicate.  
  
 The constructor:  
  
 `multimap(System::Collections::Generic::IEnumerable<Key>^ right,`  
  
 `key_compare^ pred);`  
  
 initializes the controlled sequence with the sequence designated by the enumerator `right`, with the ordering predicate `pred`. You use it to make the controlled sequence a copy of another sequence described by an enumerator, with the specified ordering predicate.  
  
## Example  
  
```  
// cliext_multimap_construct.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
int main()   
    {   
// construct an empty container   
    Mymultimap c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
    c1.insert(Mymultimap::make_value(L'a', 1));   
    c1.insert(Mymultimap::make_value(L'b', 2));   
    c1.insert(Mymultimap::make_value(L'c', 3));   
    for each (Mymultimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an ordering rule   
    Mymultimap c2 = cliext::greater_equal<wchar_t>();   
    System::Console::WriteLine("size() = {0}", c2.size());   
  
    c2.insert(c1.begin(), c1.end());   
    for each (Mymultimap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an iterator range   
    Mymultimap c3(c1.begin(), c1.end());   
    for each (Mymultimap::value_type elem in c3)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an iterator range and an ordering rule   
    Mymultimap c4(c1.begin(), c1.end(),   
        cliext::greater_equal<wchar_t>());   
    for each (Mymultimap::value_type elem in c4)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an enumeration   
    Mymultimap c5(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<   
            Mymultimap::value_type>^)%c3);   
    for each (Mymultimap::value_type elem in c5)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct with an enumeration and an ordering rule   
    Mymultimap c6(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<   
            Mymultimap::value_type>^)%c3,   
                cliext::greater_equal<wchar_t>());   
    for each (Mymultimap::value_type elem in c6)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct by copying another container   
    Mymultimap c7(c4);   
    for each (Mymultimap::value_type elem in c7)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct by copying a container handle   
    Mymultimap c8(%c3);   
    for each (Mymultimap::value_type elem in c8)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
 **size() = 0**  
 **[a 1] [b 2] [c 3]**  
**size() = 0**  
 **[c 3] [b 2] [a 1]**  
 **[a 1] [b 2] [c 3]**  
 **[c 3] [b 2] [a 1]**  
 **[a 1] [b 2] [c 3]**  
 **[c 3] [b 2] [a 1]**  
 **[c 3] [b 2] [a 1]**  
 **[a 1] [b 2] [c 3]**   
## Requirements  
 **Header:** <cliext/map>  
  
 **Namespace:** cliext  
  
## See Also  
 [multimap](../Topic/multimap%20\(STL-CLR\).md)   
 [generic_container](../vs140/multimap--generic_container--STL-CLR-.md)   
 [operator=](../vs140/multimap--operator=--STL-CLR-.md)