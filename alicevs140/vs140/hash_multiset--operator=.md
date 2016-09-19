---
title: "hash_multiset::operator="
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
ms.assetid: 639cc3f3-1ba6-4cb1-a513-3de8170d6255
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_multiset::operator=
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_multiset Class](../vs140/unordered_multiset-Class.md).  
  
 Replaces the elements of the hash_multiset with a copy of another hash_multiset.  
  
## Syntax  
  
```  
hash_multiset& operator=(  
   const hash_multiset& _Right  
);  
hash_multiset& operator=(  
   hash_multiset&& _Right  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`_Right`|The [hash_multiset](../vs140/hash_multiset-Class.md) being copied into the `hash_multiset`.|  
  
## Remarks  
 After erasing any existing elements in a `hash_multiset`, `operator=` either copies or moves the contents of `_Right` into the `hash_multiset`.  
  
## Example  
  
```  
// hash_multiset_operator_as.cpp  
// compile with: /EHsc  
#include <hash_multiset>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_multiset<int> v1, v2, v3;  
   hash_multiset<int>::iterator iter;  
  
   v1.insert(10);  
  
   cout << "v1 = " ;  
   for (iter = v1.begin(); iter != v1.end(); iter++)  
      cout << iter << " ";  
   cout << endl;  
  
   v2 = v1;  
   cout << "v2 = ";  
   for (iter = v2.begin(); iter != v2.end(); iter++)  
      cout << iter << " ";  
   cout << endl;  
  
// move v1 into v2  
   v2.clear();  
   v2 = move(v1);  
   cout << "v2 = ";  
   for (iter = v2.begin(); iter != v2.end(); iter++)  
      cout << iter << " ";  
   cout << endl;  
}  
```  
  
## Output  
  
```  
v1 = 10   
v2 = 10   
v2 = 10   
```  
  
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** std  
  
## See Also  
 [hash_multiset Class](../vs140/hash_multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)