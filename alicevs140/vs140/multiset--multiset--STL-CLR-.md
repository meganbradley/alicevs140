---
title: "multiset::multiset (STL-CLR)"
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
H1: multiset::multiset (STL/CLR)
ms.assetid: a6ddb2df-d7cd-4b12-aee7-81da1f67f57f
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::multiset (STL-CLR)
Constructs a container object.  
  
## Syntax  
  
```  
multiset();  
explicit multiset(key_compare^ pred);  
multiset(multiset<Key>% right);  
multiset(multiset<Key>^ right);  
template<typename InIter>  
    multisetmultiset(InIter first, InIter last);  
template<typename InIter>  
    multiset(InIter first, InIter last,  
        key_compare^ pred);  
multiset(System::Collections::Generic::IEnumerable<GValue>^ right);  
multiset(System::Collections::Generic::IEnumerable<GValue>^ right,  
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
  
 `multiset();`  
  
 initializes the controlled sequence with no elements, with the default ordering predicate `key_compare()`. You use it to specify an empty initial controlled sequence, with the default ordering predicate.  
  
 The constructor:  
  
 `explicit multiset(key_compare^ pred);`  
  
 initializes the controlled sequence with no elements, with the ordering predicate `pred`. You use it to specify an empty initial controlled sequence, with the specified ordering predicate.  
  
 The constructor:  
  
 `multiset(multiset<Key>% right);`  
  
 initializes the controlled sequence with the sequence `[``right``.`[begin](../vs140/multiset--begin--STL-CLR-.md)`(),` `right``.`[end](../vs140/multiset--end--STL-CLR-.md)`())`, with the default ordering predicate. You use it to specify an initial controlled sequence that is a copy of the sequence controlled by the multiset object `right`, with the default ordering predicate.  
  
 The constructor:  
  
 `multiset(multiset<Key>^ right);`  
  
 initializes the controlled sequence with the sequence `[``right``->`[begin](../vs140/multiset--begin--STL-CLR-.md)`(),` `right``->`[end](../vs140/multiset--end--STL-CLR-.md)`())`, with the default ordering predicate. You use it to specify an initial controlled sequence that is a copy of the sequence controlled by the multiset object `right`, with the default ordering predicate.  
  
 The constructor:  
  
 `template<typename InIter>`  
  
 `multiset(InIter first, InIter last);`  
  
 initializes the controlled sequence with the sequence `[``first``,` `last``)`, with the default ordering predicate. You use it to make the controlled sequence a copy of another sequence, with the default ordering predicate.  
  
 The constructor:  
  
 `template<typename InIter>`  
  
 `multiset(InIter first, InIter last,`  
  
 `key_compare^ pred);`  
  
 initializes the controlled sequence with the sequence `[``first``,` `last``)`, with the ordering predicate `pred`. You use it to make the controlled sequence a copy of another sequence, with the specified ordering predicate.  
  
 The constructor:  
  
 `multiset(System::Collections::Generic::IEnumerable<Key>^ right);`  
  
 initializes the controlled sequence with the sequence designated by the enumerator `right`, with the default ordering predicate. You use it to make the controlled sequence a copy of another sequence described by an enumerator, with the default ordering predicate.  
  
 The constructor:  
  
 `multiset(System::Collections::Generic::IEnumerable<Key>^ right,`  
  
 `key_compare^ pred);`  
  
 initializes the controlled sequence with the sequence designated by the enumerator `right`, with the ordering predicate `pred`. You use it to make the controlled sequence a copy of another sequence described by an enumerator, with the specified ordering predicate.  
  
## Example  
  
```  
// cliext_multiset_construct.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
// construct an empty container   
    Mymultiset c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an ordering rule   
    Mymultiset c2 = cliext::greater_equal<wchar_t>();   
    System::Console::WriteLine("size() = {0}", c2.size());   
  
    c2.insert(c1.begin(), c1.end());   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an iterator range   
    Mymultiset c3(c1.begin(), c1.end());   
    for each (wchar_t elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an iterator range and an ordering rule   
    Mymultiset c4(c1.begin(), c1.end(),   
        cliext::greater_equal<wchar_t>());   
    for each (wchar_t elem in c4)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an enumeration   
    Mymultiset c5(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c3);   
    for each (wchar_t elem in c5)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an enumeration and an ordering rule   
    Mymultiset c6(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c3,   
            cliext::greater_equal<wchar_t>());   
    for each (wchar_t elem in c6)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct from a generic container   
    Mymultiset c7(c4);   
    for each (wchar_t elem in c7)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another container   
    Mymultiset c8(%c3);   
    for each (wchar_t elem in c8)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
 **size() = 0**  
 **a b c**  
**size() = 0**  
 **c b a**  
 **a b c**  
 **c b a**  
 **a b c**  
 **c b a**  
 **c b a**  
 **a b c**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [multiset](../Topic/multiset%20\(STL-CLR\).md)   
 [generic_container](../vs140/multiset--generic_container--STL-CLR-.md)   
 [operator=](../vs140/multiset--operator=--STL-CLR-.md)