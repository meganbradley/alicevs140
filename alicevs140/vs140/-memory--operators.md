---
title: "&lt;memory&gt; operators"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 257e3ba9-c4c2-4ae8-9b11-b156ba9c28de
caps.latest.revision: 11
---
# &lt;memory&gt; operators
||||  
|-|-|-|  
|[operator!=](#operator_neq)|[operator&gt;](#operator_gt_)|[operator&gt;=](#operator_gt__eq)|  
|[operator&lt;](#operator_lt_)|[operator&lt;&lt;](#operator_lt__lt_)|[operator&lt;=](#operator_lt__eq)|  
|[operator==](#operator_eq_eq)|  
  
##  <a name="operator_neq"></a>  operator!=  
 Tests for inequality between objects.  
  
```  
template<class Type, class Other>  
   bool operator!=(  
      const allocator<Type>& _Left,  
      const allocator<Other>& _Right  
   ) throw();  
template<class Type1, class Del1, class Type2, class Del2>  
    bool operator!=(  
        const unique_ptr<Type1, Del1>& _Left,  
        const unique_ptr<Type2&, Del2>& _Right  
                );  
template<class Ty1, class Ty2>  
    bool operator!=(  
        const shared_ptr<Ty1>& _Left,  
        const shared_ptr<Ty2>& _Right  
   );  
  
```  
  
### Parameters  
 `_Left`  
 One of the objects to be tested for inequality.  
  
 `_Right`  
 One of the objects to be tested for inequality.  
  
 `Ty1`  
 The type controlled by the left shared pointer.  
  
 `Ty2`  
 The type controlled by the right shared pointer.  
  
### Return Value  
 **true** if the objects are not equal; **false** if objects are equal.  
  
### Remarks  
 The first template operator returns false. (All default allocators are equal.)  
  
 The second and third template operators return `!(``_Left` `==` `_Right``)`.  
  
### Example  
  
```  
// memory_op_me.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   allocator<double> Alloc;  
   vector <char>:: allocator_type v1Alloc;  
  
   if ( Alloc != v1Alloc )  
      cout << "The allocator objects Alloc & v1Alloc not are equal."  
           << endl;  
   else  
      cout << "The allocator objects Alloc & v1Alloc are equal."  
           << endl;  
}  
```  
  
  **The allocator objects Alloc & v1Alloc are equal.**    
### Example  
  
```  
// std_tr1__memory__operator_ne.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::shared_ptr<int> sp0(new int(0));   
    std::shared_ptr<int> sp1(new int(0));   
  
    std::cout << "sp0 != sp0 == " << std::boolalpha   
        << (sp0 != sp0) << std::endl;   
    std::cout << "sp0 != sp1 == " << std::boolalpha   
        << (sp0 != sp1) << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **sp0 != sp0 == false**  
**sp0 != sp1 == true**    
##  <a name="operator_eq_eq"></a>  operator==  
 Tests for equality between objects.  
  
```  
template<class Type, class Other>  
   bool operator==(  
      const allocator<Type>& _Left,  
      const allocator<Other>& _Right  
   ) throw();  
template<class Ty1, class Del1, class Ty2, class Del2>  
    bool operator==(  
        const unique_ptr<Ty1, Del1>& _Left,  
        const unique_ptr<Ty2, Del2>& _Right  
    );  
template<class Ty1, class Ty2>  
    bool operator==(  
      const shared_ptr<Ty1>& _Left;,  
      const shared_ptr<Ty2>& _Right  
   );  
  
```  
  
### Parameters  
 `_Left`  
 One of the objects to be tested for equality.  
  
 `_Right`  
 One of the objects to be tested for equality.  
  
 `Ty1`  
 The type controlled by the left shared pointer.  
  
 `Ty2`  
 The type controlled by the right shared pointer.  
  
### Return Value  
 `true` if the objects are equal, `false` if objects are not equal.  
  
### Remarks  
 The first template operator returns true. (All default allocators are equal.)  
  
 The second and third template operators return `_Left.get() == _Right.get()`.  
  
### Example  
  
```  
// memory_op_eq.cpp  
// compile with: /EHsc  
#include <memory>  
#include <iostream>  
#include <vector>  
  
using namespace std;  
  
int main( )   
{  
   allocator<char> Alloc;  
   vector <int>:: allocator_type v1Alloc;  
  
   allocator<char> cAlloc(Alloc);   
   allocator<int> cv1Alloc(v1Alloc);  
  
   if ( cv1Alloc == v1Alloc )  
      cout << "The allocator objects cv1Alloc & v1Alloc are equal."  
           << endl;  
   else  
      cout << "The allocator objects cv1Alloc & v1Alloc are not equal."  
           << endl;  
  
   if ( cAlloc == Alloc )  
      cout << "The allocator objects cAlloc & Alloc are equal."  
           << endl;  
   else  
      cout << "The allocator objects cAlloc & Alloc are not equal."  
           << endl;  
}  
```  
  
  **The allocator objects cv1Alloc & v1Alloc are equal.**  
**The allocator objects cAlloc & Alloc are equal.**    
### Example  
  
```  
// std_tr1__memory__operator_eq.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::shared_ptr<int> sp0(new int(0));   
    std::shared_ptr<int> sp1(new int(0));   
  
    std::cout << "sp0 == sp0 == " << std::boolalpha   
        << (sp0 == sp0) << std::endl;   
    std::cout << "sp0 == sp1 == " << std::boolalpha   
        << (sp0 == sp1) << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **sp0 == sp0 == true**  
**sp0 == sp1 == false**    
##  <a name="operator_gt__eq"></a>  operator&gt;=  
 Tests for one object being greater than or equal to a second object.  
  
```  
template<class Type1, class Del1, class Type2, class Del2>  
    bool operator>=(  
        const unique_ptr<Type1, Del1>& _Left,  
        const unique_ptr<Type2, Del2>& _Right  
    );  
template<class Ty1, class Ty2>  
    bool operator>=(  
        const shared_ptr<Ty1>& _Left,  
        const shared_ptr<Ty2>& _Right  
                );  
```  
  
### Parameters  
 `_Left`  
 One of the objects to be compared.  
  
 `_Right`  
 One of the objects to be compared.  
  
 `Ty1`  
 The type controlled by the left shared pointer.  
  
 `Ty2`  
 The type controlled by the right shared pointer.  
  
### Remarks  
 The template operators return `_Left``.get() >=` `_Right``.get()`.  
  
##  <a name="operator_lt_"></a>  operator&lt;  
 Tests for one object being less than a second object.  
  
```  
template<class Type1, class Del1, class Type2, class Del2>  
    bool operator<(  
        const unique_ptr<Type1, Del1>& _Left,  
        const unique_ptr<Type2&, Del2>& _Right  
    );  
template<class Ty1, class Ty2>  
    bool operator<(  
        const shared_ptr<Ty1>& _Left,  
        const shared_ptr<Ty2>& _Right  
    );  
  
```  
  
### Parameters  
 `_Left`  
 One of the objects to be compared.  
  
 `_Right`  
 One of the objects to be compared.  
  
 `Ty1`  
 The type controlled by the left pointer.  
  
 `Ty2`  
 The type controlled by the right pointer.  
  
##  <a name="operator_lt__eq"></a>  operator&lt;=  
 Tests for one object being less than or equal to a second object.  
  
```  
template<class Type1, class Del1, class Type2, class Del2>  
    bool operator<=(  
        const unique_ptr<Type1, Del1>& _Left,  
        const unique_ptr<Type2&, Del2>& _Right  
    );  
template<class Ty1, class Ty2>  
    bool operator<=(  
        const shared_ptr<Ty1>& _Left,  
        const shared_ptr<Ty2>& _Right  
);  
```  
  
### Parameters  
 `_Left`  
 One of the objects to be compared.  
  
 `_Right`  
 One of the objects to be compared.  
  
 `Ty1`  
 The type controlled by the left shared pointer.  
  
 `Ty2`  
 The type controlled by the right shared pointer.  
  
### Remarks  
 The template operators return `_Left``.get() <=` `_Right``.get()`  
  
##  <a name="operator_gt_"></a>  operator&gt;  
 Tests for one object being greater than a second object.  
  
```  
template<class Ty1, class Del1, class Ty2, class Del2>  
    bool operator>(  
        const unique_ptr<Ty1, Del1>& _Left,  
        const unique_ptr<Ty2&, Del2gt;& _Right  
    );  
template<class Ty1, class Ty2>  
    bool operator>(  
        const shared_ptr<Ty1>& _Left,  
        const shared_ptr<Ty2>& _Right  
    );  
```  
  
### Parameters  
 `_Left`  
 One of the objects to be compared.  
  
 `_Right`  
 One of the objects to be compared.  
  
 `Ty1`  
 The type controlled by the left shared pointer.  
  
 `Ty2`  
 The type controlled by the right shared pointer.  
  
##  <a name="operator_lt__lt_"></a>  operator&lt;&lt;  
 shared_ptr inserter.  
  
```  
template<class Elem, class Tr, class Ty>  
    std::basic_ostream<Elem, Tr>& operator<<(std::basic_ostream<Elem, Tr>& out,  
    shared_ptr<Ty>& sp);  
```  
  
### Parameters  
 `Elem`  
 The type of the stream element.  
  
 `Tr`  
 The type the stream element traits.  
  
 `Ty`  
 The type controlled by the shared pointer.  
  
 `out`  
 The output stream.  
  
 `sp`  
 The shared pointer.  
  
### Remarks  
 The template function returns `out << sp.get()`.  
  
### Example  
  
```  
// std_tr1__memory__operator_sl.cpp   
// compile with: /EHsc   
#include <memory>   
#include <iostream>   
  
int main()   
    {   
    std::shared_ptr<int> sp0(new int(5));   
  
    std::cout << "sp0 == " << sp0 << " (varies)" << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **sp0 == 3f3040 (varies)**    
## See Also  
 [&lt;memory&gt;](../vs140/-memory-.md)