---
title: "unary_function Struct"
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
ms.assetid: 04c2fbdc-c1f6-48ed-b6cc-292a6d484627
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unary_function Struct
An empty base struct that defines types that may be inherited by derived classes that provides a unary function object.  
  
## Syntax  
  
```  
template<class Arg, class Result>    struct unary_function {       typedef Arg argument_type;       typedef Result result_type;    };  
  
```  
  
## Remarks  
 The template struct serves as a base for classes that define a member function of the form **result_type**`operator()`( **constargument_type&**) **const**.  
  
 All such derived unary functions can refer to their sole argument type as **argument_type** and their return type as **result_type**.  
  
## Example  
  
```  
// functional_unary_function.cpp  
// compile with: /EHsc  
#include <vector>  
#include <functional>  
#include <algorithm>  
#include <iostream>  
  
using namespace std;  
  
// Creation of a user-defined function object  
// that inherits from the unary_function base class  
class greaterthan10: unary_function<int, bool>  
{  
public:  
    result_type operator()(argument_type i)  
    {  
        return (result_type)(i > 10);  
    }  
};  
  
int main()  
{  
    vector<int> v1;  
    vector<int>::iterator Iter;  
  
    int i;  
    for (i = 0; i <= 5; i++)  
    {  
        v1.push_back(5 * i);  
    }  
  
    cout << "The vector v1 = ( " ;  
    for (Iter = v1.begin(); Iter != v1.end(); Iter++)  
        cout << *Iter << " ";  
    cout << ")" << endl;  
  
    vector<int>::iterator::difference_type result1;  
    result1 = count_if(v1.begin(), v1.end(), greaterthan10());  
    cout << "The number of elements in v1 greater than 10 is: "  
         << result1 << "." << endl;  
}  
\* Output:   
The vector v1 = ( 0 5 10 15 20 25 )  
The number of elements in v1 greater than 10 is: 3.  
*\  
```  
  
## Requirements  
 **Header:** <functional\>  
  
 **Namespace:** std  
  
## See Also  
 [unary_function<> Structure Sample](../vs140/unary_function---Structure.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)