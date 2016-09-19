---
title: "hash_multiset::count"
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
ms.assetid: 0bb4d4df-33e2-44a4-a76a-0e376791f88b
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multiset::count
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_multiset Class](../vs140/unordered_multiset-Class.md).  
  
 Returns the number of elements in a hash_multiset whose key matches a parameter-specified key.  
  
## Syntax  
  
```  
  
      size_type count(  
   const Key& _Key  
) const;  
```  
  
#### Parameters  
 `_Key`  
 The key of the elements to be matched from the hash_multiset.  
  
## Return Value  
 The number of elements in the hash_multiset with the parameter-specified key.  
  
## Remarks  
 The member function returns the number of elements in the following range:  
  
 [`lower_bound` (_`Key` ), `upper_bound` (\_`Key` ) ).  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
 The following example demonstrates the use of the hash_multiset::count member function.  
  
```  
// hash_multiset_count.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
    using namespace stdext;  
    hash_multiset<int> hms1;  
    hash_multiset<int>::size_type i;  
  
    hms1.insert(1);  
    hms1.insert(1);  
  
    // Keys do not need to be unique in hash_multiset,  
    // so duplicates may exist.  
    i = hms1.count(1);  
    cout << "The number of elements in hms1 with a sort key of 1 is: "  
         << i << "." << endl;  
  
    i = hms1.count(2);  
    cout << "The number of elements in hms1 with a sort key of 2 is: "  
         << i << "." << endl;  
}  
```  
  
 **The number of elements in hms1 with a sort key of 1 is: 2.**  
**The number of elements in hms1 with a sort key of 2 is: 0.**   
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_multiset Class](../vs140/hash_multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)