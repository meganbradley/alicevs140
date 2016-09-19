---
title: "queue::queue (STL-CLR)"
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
H1: queue::queue (STL/CLR)
ms.assetid: 6106c07f-d5eb-4f0b-82df-ee4e2e751047
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# queue::queue (STL-CLR)
Constructs a container adapter object.  
  
## Syntax  
  
```  
queue();  
queue(queue<Value, Container>% right);  
queue(queue<Value, Container>^ right);  
explicit queue(container_type% wrapped);  
```  
  
#### Parameters  
 right  
 Object to copy.  
  
 wrapped  
 Wrapped container to use.  
  
## Remarks  
 The constructor:  
  
 `queue();`  
  
 creates an empty wrapped container. You use it to specify an empty initial controlled sequence.  
  
 The constructor:  
  
 `queue(queue<Value, Container>% right);`  
  
 creates a wrapped container that is a copy of `right.get_container()`. You use it to specify an initial controlled sequence that is a copy of the sequence controlled by the queue object `right`.  
  
 The constructor:  
  
 `queue(queue<Value, Container>^ right);`  
  
 creates a wrapped container that is a copy of `right->get_container()`. You use it to specify an initial controlled sequence that is a copy of the sequence controlled by the queue object `*right`.  
  
 The constructor:  
  
 `explicit queue(container_type wrapped);`  
  
 uses the existing container `wrapped` as the wrapped container. You use it to construct a queue from an existing container.  
  
## Example  
  
```  
// cliext_queue_construct.cpp   
// compile with: /clr   
#include <cliext/queue>   
#include <cliext/list>   
  
typedef cliext::queue<wchar_t> Myqueue;   
typedef cliext::list<wchar_t> Mylist;   
typedef cliext::queue<wchar_t, Mylist> Myqueue_list;   
int main()   
    {   
// construct an empty container   
    Myqueue c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
// construct from an underlying container   
    Mylist v2(5, L'x');   
    Myqueue_list c2(v2);       
    for each (wchar_t elem in c2.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another container   
    Myqueue_list c3(c2);   
    for each (wchar_t elem in c3.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another container through handle   
    Myqueue_list c4(%c2);   
    for each (wchar_t elem in c4.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
 **size() = 0**  
 **x x x x x**  
 **x x x x x**  
 **x x x x x**   
## Requirements  
 **Header:** <cliext/queue>  
  
 **Namespace:** cliext  
  
## See Also  
 [queue](../Topic/queue%20\(STL-CLR\).md)   
 [assign](../vs140/queue--assign--STL-CLR-.md)   
 [generic_container](../vs140/queue--generic_container--STL-CLR-.md)   
 [operator=](../vs140/queue--operator=--STL-CLR-.md)