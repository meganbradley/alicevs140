---
title: "range_adapter::range_adapter (STL-CLR)"
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
H1: range_adapter::range_adapter (STL/CLR)
ms.assetid: b16af13f-3358-4e82-927d-d0d4986bcb18
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# range_adapter::range_adapter (STL-CLR)
Constructs an adapter object.  
  
## Syntax  
  
```  
range_adapter();  
range_adapter(range_adapter<Iter>% right);  
range_adapter(range_adapter<Iter>^ right);  
range_adapter(Iter first, Iter last);  
```  
  
#### Parameters  
 first  
 First iterator to wrap.  
  
 last  
 Second iterator to wrap.  
  
 right  
 Object to copy.  
  
## Remarks  
 The constructor:  
  
 `range_adapter();`  
  
 initializes the stored iterator pair with default constructed iterators.  
  
 The constructor:  
  
 `range_adapter(range_adapter<Iter>% right);`  
  
 initializes the stored iterator pair by copying the pair stored in `right`.  
  
 The constructor:  
  
 `range_adapter(range_adapter<Iter>^ right);`  
  
 initializes the stored iterator pair by copying the pair stored in `*right`.  
  
 The constructor:  
  
 `range_adapter(Iter^ first, last);`  
  
 initializes the stored iterator pair with `first` and `last`.  
  
## Example  
  
```  
// cliext_range_adapter_construct.cpp   
// compile with: /clr   
#include <cliext/adapter>   
#include <cliext/deque>   
  
typedef cliext::deque<wchar_t> Mycont;   
typedef cliext::range_adapter<Mycont::iterator> Myrange;   
int main()   
    {   
    cliext::deque<wchar_t> d1;   
    d1.push_back(L'a');   
    d1.push_back(L'b');   
    d1.push_back(L'c');   
  
// construct an empty adapter   
    Myrange c1;   
  
// construct with an iterator pair   
    Myrange c2(d1.begin(), d1.end());   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another adapter   
    Myrange c3(c2);   
    for each (wchar_t elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying an adapter handle   
    Myrange c4(%c3);   
    for each (wchar_t elem in c4)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    return (0);   
    }  
  
```  
  
  **a b c**  
 **a b c**  
 **a b c**   
## Requirements  
 **Header:** <cliext/adapter>  
  
 **Namespace:** cliext  
  
## See Also  
 [range_adapter](../vs140/range_adapter--STL-CLR-.md)   
 [operator=](../vs140/range_adapter--operator=--STL-CLR-.md)