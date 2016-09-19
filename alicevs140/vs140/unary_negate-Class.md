---
title: "unary_negate Class"
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
ms.assetid: e3b86eec-3205-49b9-ab83-f55225af4e0c
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unary_negate Class
A template class providing a member function that negates the return value of a specified unary function.  
  
## Syntax  
  
```  
template<class Predicate>    class unary_negate       : public unary_function<          typename Predicate::argument_type,          bool>     {    public:    explicit unary_negate(       const Predicate&  _Func    );    bool operator()(       const typename Predicate::argument_type&  _Left  ) const;    };  
  
```  
  
#### Parameters  
 `_Func`  
 The unary function to be negated.  
  
 `_Left`  
 The operand of the unary function to be negated.  
  
## Return Value  
 The negation of the unary function.  
  
## Remarks  
 The template class stores a copy of a unary function object _                *Func.* It defines its member function `operator()` as returning **!**\_                *Func(_Left).*  
  
 The constructor of `unary_negate` is rarely used directly. The helper function [not1](../vs140/-functional--functions.md#not1_function) provides an easier way to declare and use the **unary_negator** adaptor predicate.  
  
## Example  
  
```  
// functional_unary_negate.cpp  
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
    for (i = 0; i <= 7; i++)  
    {  
        v1.push_back(5 * i);  
    }  
  
    cout << "The vector v1 = ( ";  
    for (Iter = v1.begin(); Iter != v1.end(); Iter++)  
        cout << *Iter << " ";  
    cout << ")" << endl;  
  
    vector<int>::iterator::difference_type result1;  
    // Count the elements greater than 10  
    result1 = count_if(v1.begin(), v1.end(), bind2nd(greater<int>(), 10));  
    cout << "The number of elements in v1 greater than 10 is: "  
         << result1 << "." << endl;  
  
    vector<int>::iterator::difference_type result2;  
    // Use the negator to count the elements less than or equal to 10  
    result2 = count_if(v1.begin(), v1.end(),  
        unary_negate<binder2nd <greater<int> > >(bind2nd(greater<int>(),10)));  
  
    // The following helper function not1 also works for the above line  
    // not1(bind2nd(greater<int>(), 10)));  
  
    cout << "The number of elements in v1 not greater than 10 is: "  
         << result2 << "." << endl;  
}  
/* Output:  
The vector v1 = ( 0 5 10 15 20 25 30 35 )  
The number of elements in v1 greater than 10 is: 5.  
The number of elements in v1 not greater than 10 is: 3.  
*/  
```  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)