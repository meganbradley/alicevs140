---
title: "accumulate"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9908525b-967c-402d-9ee9-aadacc241efc
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accumulate
Computes the sum of all the elements in a specified range including some initial value by computing successive partial sums or computes the result of successive partial results similarly obtained from using a specified binary operation other than the sum.  
  
## Syntax  
  
```  
  
      template<class InputIterator, class Type>  
   Type accumulate(  
      InputIterator _First,   
      InputIterator _Last,   
      Type _Val  
   );  
template<class InputIterator, class Type, class BinaryOperation>  
   Type accumulate(  
      InputIterator _First,   
      InputIterator _Last,   
      Type _Val,   
      BinaryOperation _Binary_op  
   );  
```  
  
#### Parameters  
 `_First`  
 An input iterator addressing the first element in the range to be summed or combined according to a specified binary operation.  
  
 `_Last`  
 An input iterator addressing the last element in the range to be summed or combined according to a specified binary operation that is one position beyond the final element actually included in the iterated accumulation.  
  
 `_Val`  
 An initial value to which each element is in turn added or combined with according to a specified binary operation.  
  
 `_Binary_op`  
 The binary operation that is to be applied to the each element in the specified range and the result of its previous applications.  
  
## Return Value  
 The sum of `_Val` and all the elements in the specified range for the first template function, or, for the second template function, the result of applying the binary operation specified, instead of the sum operation, to (*PartialResult, \*Iter*), where *PartialResult* is the result of previous applications of the operation and `Iter` is an iterator pointing to an element in the range.  
  
## Remarks  
 The initial value insures that there will be a well-defined result when the range is empty, in which case `_Val` is returned. The binary operation does not need to be associative or commutative. The result is initialized to the initial value `_Val` and then *result* = `_Binary_op` (*result*, **\***`Iter`) is calculated iteratively through the range, where `Iter` is an iterator pointing to successive element in the range. The range must be valid and the complexity is linear with the size of the range. The return type of the binary operator must be convertible to **Type** to ensure closure during the iteration.  
  
## Example  
  
```  
// numeric_accum.cpp  
// compile with: /EHsc  
#include <vector>  
#include <numeric>  
#include <functional>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   vector <int> v1, v2(20);  
   vector <int>::iterator iter1, iter2;  
  
   int i;  
   for (i = 1; i < 21; i++)  
   {  
      v1.push_back(i);  
   }  
  
   cout << "The original vector v1 is:\n ( " ;  
   for (iter1 = v1.begin(); iter1 != v1.end(); iter1++)  
      cout << *iter1 << " ";  
   cout << ")." << endl;  
  
   // The first member function for the accumulated sum  
   int total;  
   total = accumulate(v1.begin(), v1.end(), 0);  
  
   cout << "The sum of the integers from 1 to 20 is: "  
        << total << "." << endl;  
  
   // Constructing a vector of partial sums  
   int j = 0, partotal;  
   for (iter1 = v1.begin(); iter1 != v1.end(); iter1++)  
   {  
      partotal = accumulate(v1.begin(), iter1 + 1, 0);  
      v2[j] = partotal;  
      j++;  
   }  
  
   cout << "The vector of partial sums is:\n ( " ;  
   for (iter2 = v2.begin(); iter2 != v2.end(); iter2++)  
      cout << *iter2 << " ";  
   cout << ")." << endl << endl;  
  
   // The second member function for the accumulated product  
   vector <int> v3, v4(10);  
   vector <int>::iterator iter3, iter4;  
  
   int s;  
   for (s = 1; s < 11; s++)  
   {  
      v3.push_back(s);  
   }  
  
   cout << "The original vector v3 is:\n ( " ;  
   for (iter3 = v3.begin(); iter3 != v3.end(); iter3++)  
      cout << *iter3 << " ";  
   cout << ")." << endl;  
  
   int ptotal;  
   ptotal = accumulate(v3.begin(), v3.end(), 1, multiplies<int>());  
  
   cout << "The product of the integers from 1 to 10 is: "  
        << ptotal << "." << endl;  
  
   // Constructing a vector of partial products  
   int k = 0, ppartotal;  
   for (iter3 = v3.begin(); iter3 != v3.end(); iter3++) {  
      ppartotal = accumulate(v3.begin(), iter3 + 1, 1, multiplies<int>());  
      v4[k] = ppartotal;  
      k++;  
   }  
  
   cout << "The vector of partial products is:\n ( " ;  
   for (iter4 = v4.begin(); iter4 != v4.end(); iter4++)  
      cout << *iter4 << " ";  
   cout << ")." << endl;  
}  
```  
  
 **The original vector v1 is:**  
 **( 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 ).**  
**The sum of the integers from 1 to 20 is: 210.**  
**The vector of partial sums is:**  
 **( 1 3 6 10 15 21 28 36 45 55 66 78 91 105 120 136 153 171 190 210 ).**  
**The original vector v3 is:**  
 **( 1 2 3 4 5 6 7 8 9 10 ).**  
**The product of the integers from 1 to 10 is: 3628800.**  
**The vector of partial products is:**  
 **( 1 2 6 24 120 720 5040 40320 362880 3628800 ).**   
## Requirements  
 **Header:** <numeric\>  
  
 **Namespace:** std  
  
## See Also  
 [accumulate, copy, and vector::push_back](../vs140/accumulate--copy--and-vector--push_back.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)