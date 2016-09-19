---
title: "multiset::emplace"
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
ms.assetid: 0c32f77f-2e6b-4411-982d-c3afd39fe0a9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::emplace
Inserts an element constructed in place (no copy or move operations are performed), with a placement hint.  
  
## Syntax  
  
```  
template<class... Args>  
   iterator emplace(  
      Args&&... args);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`args`|The arguments forwarded to construct an element to be inserted into the multiset.|  
  
## Return Value  
 An iterator to the newly inserted element.  
  
## Remarks  
 No references to container elements are invalidated by this function, but it may invalidate all iterators to the container.  
  
 During emplacement, if an exception is thrown, the container's state is not modified.  
  
## Example  
  
```cpp  
// multiset_emplace.cpp  
// compile with: /EHsc  
#include <set>  
#include <string>  
#include <iostream>  
  
using namespace std;  
  
template <typename S> void print(const S& s) {  
    cout << s.size() << " elements: ";  
  
    for (const auto& p : s) {  
        cout << "(" << p << ") ";  
    }  
  
    cout << endl;  
}  
  
int main()  
{  
    multiset<string> s1;  
  
    s1.emplace("Anna");  
    s1.emplace("Bob");  
    s1.emplace("Carmine");  
  
    cout << "multiset modified, now contains ";  
    print(s1);  
    cout << endl;  
  
    s1.emplace("Bob");  
  
    cout << "multiset modified, now contains ";  
    print(s1);  
    cout << endl;  
}  
  
```  
  
## Output  
  
```  
  
multiset modified, now contains 3 elements: (Anna) (Bob) (Carmine)  
  
multiset modified, now contains 4 elements: (Anna) (Bob) (Bob) (Carmine)  
```  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [<set\>](../vs140/-set-.md)   
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)