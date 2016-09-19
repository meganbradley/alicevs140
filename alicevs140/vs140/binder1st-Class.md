---
title: "binder1st Class"
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
ms.assetid: 6b8ee343-c82f-48f8-867d-06f9d1d324c0
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# binder1st Class
A template class providing a constructor that converts a binary function object into a unary function object by binding the first argument of the binary function to a specified value.  
  
## Syntax  
  
```  
template<class Operation>  
class binder1st  
   : public unary_function <  
      typename Operation::second_argument_type,  
      typename Operation::result_type>   
  {  
   public:  
   typedef typename Operation::argument_type argument_type;  
   typedef typename Operation::result_type result_type;  
   binder1st(  
      const Operation & _Func,  
      const typename Operation::first_argument_type& _Left  
   );  
   result_type operator()(  
      const argument_type& _Right  
   ) const;  
   result_type operator()(  
      const argument_type& _Right  
   ) const;  
   protected:  
   Operation op;  
   typename Operation::first_argument_type value;  
   };  
```  
  
#### Parameters  
 `_Func`  
 The binary function object to be converted to a unary function object.  
  
 `_Left`  
 The value to which the first argument of the binary function object is to be bound.  
  
 `_Right`  
 The value of the argument that the adapted binary object compares to the fixed value of the second argument.  
  
## Return Value  
 The unary function object that results from binding the first argument of the binary function object to the value `_Left.`  
  
## Remarks  
 The template class stores a copy of a binary function object `_Func` in **op**, and a copy of `_Left` in **value**. It defines its member function `operator()` as returning **op**( **value**, `_Right`).  
  
 If `_Func` is an object of type **Operation** and `c` is a constant , then [bind1st](../vs140/-functional--functions.md#bind1st_function) ( `_Func`, `c` ) is equivalent to the `binder1st` class constructor `binder1st`< **Operation**> ( `_Func`, `c` ) and more convenient.  
  
## Example  
  
```  
// functional_binder1st.cpp  
// compile with: /EHsc  
#include <vector>  
#include <functional>  
#include <algorithm>  
#include <iostream>  
  
using namespace std;  
  
int main()  
{  
    vector<int> v1;  
    vector<int>::iterator Iter;  
  
    int i;  
    for (i = 0; i <= 5; i++)  
    {  
        v1.push_back(5 * i);  
    }  
  
    cout << "The vector v1 = ( ";  
    for (Iter = v1.begin(); Iter != v1.end(); Iter++)  
        cout << *Iter << " ";  
    cout << ")" << endl;  
  
    // Count the number of integers > 10 in the vector  
    vector<int>::iterator::difference_type result1;  
    result1 = count_if(v1.begin(), v1.end(),  
        binder1st<less<int> >(less<int>(), 10));  
    cout << "The number of elements in v1 greater than 10 is: "  
         << result1 << "." << endl;  
  
    // Compare use of binder2nd fixing 2nd argument:  
    // count the number of integers < 10 in the vector  
    vector<int>::iterator::difference_type result2;  
    result2 = count_if(v1.begin(), v1.end(),  
        binder2nd<less<int> >(less<int>(), 10));  
    cout << "The number of elements in v1 less than 10 is: "  
         << result2 << "." << endl;  
}  
\* Output:   
The vector v1 = ( 0 5 10 15 20 25 )  
The number of elements in v1 greater than 10 is: 3.  
The number of elements in v1 less than 10 is: 2.  
*\  
```  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)