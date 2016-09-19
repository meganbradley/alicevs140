---
title: "hash_set::count"
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
ms.assetid: 93e487d7-1768-4800-a5ac-ea0f9efce744
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_set::count
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Returns the number of elements in a hash_set whose key matches a parameter-specified key.  
  
## Syntax  
  
```  
  
      size_type count(  
   const Key& _Key  
) const;  
```  
  
#### Parameters  
 `_Key`  
 The key of the elements to be matched from the hash_set.  
  
## Return Value  
 1 if the hash_set contains an element whose sort key matches the parameter key.  
  
 0 if the hash_set does not contain an element with a matching key.  
  
## Remarks  
 The member function returns the number of elements in the following range:  
  
 [**lower_bound** (_*Key* ), **upper_bound** (\_*Key* ) ).  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 The following example demonstrates the use of the hash_set::count member function.  
  
```  
// hash_set_count.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
    using namespace stdext;  
    hash_set<int> hs1;  
    hash_set<int>::size_type i;  
  
    hs1.insert(1);  
    hs1.insert(1);  
  
    // Keys must be unique in hash_set, so duplicates are ignored.  
    i = hs1.count(1);  
    cout << "The number of elements in hs1 with a sort key of 1 is: "  
         << i << "." << endl;  
  
    i = hs1.count(2);  
    cout << "The number of elements in hs1 with a sort key of 2 is: "  
         << i << "." << endl;  
}  
```  
  
 **The number of elements in hs1 with a sort key of 1 is: 1.**  
**The number of elements in hs1 with a sort key of 2 is: 0.**   
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_set Class](../vs140/hash_set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)