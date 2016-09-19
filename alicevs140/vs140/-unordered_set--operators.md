---
title: "&lt;unordered_set&gt; operators"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8653eea6-12f2-4dd7-aa2f-db38a71599a0
caps.latest.revision: 7
---
# &lt;unordered_set&gt; operators
|||||  
|-|-|-|-|  
|[operator!= (unordered_set)](#operator_neq)|[operator== (unordered_set)](#operator_eq_eq)|[operator!= (unordered_multiset)](#operator_neq_unordered_multiset)|[operator== (unordered_multiset)](#operator_eq_eq_unordered_multiset)|  
  
##  <a name="operator_neq"></a>  operator!=  
 Tests whether the [unordered_set](../vs140/unordered_set-Class.md) object on the left side of the operator is not equal to the unordered_set object on the right side.  
  
```  
bool operator!=(    const unordered_set <Key, Hash, Pred, Allocator>&  _Left ,    const unordered_set <Key, Hash, Pred, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `unordered_set`.  
  
 `_Right`  
 An object of type `unordered_set`.  
  
### Return Value  
 `true` if the unordered_sets are not equal; `false` if they are equal.  
  
### Remarks  
 The comparison between unordered_set objects is not affected by the arbitrary order in which they store their elements. Two unordered_sets are equal if they have the same number of elements and the elements in one container are a permutation of the elements in the other container. Otherwise, they are unequal.  
  
### Example  
  
```cpp  
  
// unordered_set_ne.cpp   
// compile by using: cl.exe /EHsc /nologo /W4 /MTd   
#include <unordered_set>   
#include <iostream>   
#include <ios>  
  
int main()   
{   
    using namespace std;  
  
    unordered_set<char> c1, c2, c3;  
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
    c2.insert('c');   
    c2.insert('a');   
    c2.insert('d');   
  
    c3.insert('c');   
    c3.insert('a');   
    c3.insert('b');   
  
   cout << boolalpha;  
   cout << "c1 != c2: " << (c1 != c2) << endl;   
   cout << "c1 != c3: " << (c1 != c3) << endl;   
   cout << "c2 != c3: " << (c2 != c3) << endl;   
  
    return (0);   
}  
  
```  
  
  **Output:**  
  
 `c1 != c2: true`  
  
 `c1 != c3: false`  
  
 `c2 != c3: true`  
  
##  <a name="operator_eq_eq"></a>  operator==  
 Tests whether the [unordered_set](../vs140/unordered_set-Class.md) object on the left side of the operator is equal to the unordered_set object on the right side.  
  
```  
bool operator==(    const unordered_set <Key, Hash, Pred, Allocator>&  _Left ,    const unordered_set <Key, Hash, Pred, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `unordered_set`.  
  
 `_Right`  
 An object of type `unordered_set`.  
  
### Return Value  
 `true` if the unordered_sets are equal; `false` if they are not equal.  
  
### Remarks  
 The comparison between unordered_set objects is not affected by the arbitrary order in which they store their elements. Two unordered_sets are equal if they have the same number of elements and the elements in one container are a permutation of the elements in the other container. Otherwise, they are unequal.  
  
### Example  
  
```cpp  
  
// unordered_set_eq.cpp   
// compile by using: cl.exe /EHsc /nologo /W4 /MTd   
#include <unordered_set>   
#include <iostream>   
#include <ios>  
  
int main()   
{   
    using namespace std;  
  
    unordered_set<char> c1, c2, c3;  
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
  
    c2.insert('c');   
    c2.insert('a');   
    c2.insert('d');   
  
    c3.insert('c');   
    c3.insert('a');   
    c3.insert('b');   
  
   cout << boolalpha;  
   cout << "c1 == c2: " << (c1 == c2) << endl;   
   cout << "c1 == c3: " << (c1 == c3) << endl;   
   cout << "c2 == c3: " << (c2 == c3) << endl;   
  
    return (0);   
}  
  
```  
  
  **Output:**  
  
 `c1 == c2: false`  
  
 `c1 == c3: true`  
  
 `c2 == c3: false`  
  
##  <a name="operator_neq_unordered_multiset"></a>  operator!=  
 Tests whether the [unordered_multiset](../vs140/unordered_multiset-Class.md) object on the left side of the operator is not equal to the unordered_multiset object on the right side.  
  
```  
bool operator!=(    const unordered_multiset <Key, Hash, Pred, Allocator>&  _Left ,    const unordered_multiset <Key, Hash, Pred, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `unordered_multiset`.  
  
 `_Right`  
 An object of type `unordered_multiset`.  
  
### Return Value  
 `true` if the unordered_multisets are not equal; `false` if they are equal.  
  
### Remarks  
 The comparison between unordered_multiset objects is not affected by the arbitrary order in which they store their elements. Two unordered_multisets are equal if they have the same number of elements and the elements in one container are a permutation of the elements in the other container. Otherwise, they are unequal.  
  
### Example  
  
```cpp  
// unordered_multiset_ne.cpp   
// compile by using: cl.exe /EHsc /nologo /W4 /MTd   
#include <unordered_set>   
#include <iostream>   
#include <ios>  
  
int main()   
{   
    using namespace std;  
  
    unordered_multiset<char> c1, c2, c3;  
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
    c1.insert('c');   
  
    c2.insert('c');   
    c2.insert('c');   
    c2.insert('a');   
    c2.insert('d');   
  
    c3.insert('c');   
    c3.insert('c');   
    c3.insert('a');   
    c3.insert('b');   
  
   cout << boolalpha;  
   cout << "c1 != c2: " << (c1 != c2) << endl;   
   cout << "c1 != c3: " << (c1 != c3) << endl;   
   cout << "c2 != c3: " << (c2 != c3) << endl;   
  
    return (0);   
}  
  
```  
  
  **Output:**  
  
 `c1 != c2: true`  
  
 `c1 != c3: false`  
  
 `c2 != c3: true`  
  
##  <a name="operator_eq_eq_unordered_multiset"></a>  operator==  
 Tests whether the [unordered_multiset](../vs140/unordered_multiset-Class.md) object on the left side of the operator is equal to the unordered_multiset object on the right side.  
  
```  
bool operator==(    const unordered_multiset <Key, Hash, Pred, Allocator>&  _Left ,    const unordered_multiset <Key, Hash, Pred, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `unordered_multiset`.  
  
 `_Right`  
 An object of type `unordered_multiset`.  
  
### Return Value  
 `true` if the unordered_multisets are equal; `false` if they are not equal.  
  
### Remarks  
 The comparison between unordered_multiset objects is not affected by the arbitrary order in which they store their elements. Two unordered_multisets are equal if they have the same number of elements and the elements in one container are a permutation of the elements in the other container. Otherwise, they are unequal.  
  
### Example  
  
```cpp  
// unordered_multiset_eq.cpp   
// compile by using: cl.exe /EHsc /nologo /W4 /MTd   
#include <unordered_set>   
#include <iostream>   
#include <ios>  
  
int main()   
{   
    using namespace std;  
  
    unordered_multiset<char> c1, c2, c3;  
  
    c1.insert('a');   
    c1.insert('b');   
    c1.insert('c');   
    c1.insert('c');   
  
    c2.insert('c');   
    c2.insert('c');   
    c2.insert('a');   
    c2.insert('d');   
  
    c3.insert('c');   
    c3.insert('c');   
    c3.insert('a');   
    c3.insert('b');   
  
   cout << boolalpha;  
   cout << "c1 == c2: " << (c1 == c2) << endl;   
   cout << "c1 == c3: " << (c1 == c3) << endl;   
   cout << "c2 == c3: " << (c2 == c3) << endl;   
  
    return (0);   
}  
  
```  
  
  **Output:**  
  
 `c1 == c2: false`  
  
 `c1 == c3: true`  
  
 `c2 == c3: false`  
  
## See Also  
 [&lt;unordered_set&gt;](../vs140/-unordered_set-.md)