---
title: "log (&lt;valarray&gt;)"
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
ms.assetid: f9c478b6-42d6-4329-b91d-9dee74025528
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# log (&lt;valarray&gt;)
Operates on the elements of an input valarray, returning a valarray whose elements are equal to the natural logarithm of the elements of the input valarray.  
  
## Syntax  
  
```  
  
   template<class Type>  
valarray<Type> log(  
   const valarray<Type>& _Left  
);  
```  
  
#### Parameters  
 `_Left`  
 The input valarray whose elements are to be operated on by the member function.  
  
## Return Value  
 A valarray whose elements are equal to the absolute value of the elements of the input valarray.  
  
## Example  
  
```  
// valarray_log.cpp  
// compile with: /EHsc  
#include <valarray>  
#include <iostream>  
#include <iomanip>  
  
int main( )  
{  
   using namespace std;  
   int i;  
  
   valarray<double> va1 ( 9 );  
   for (i = 0 ; i < 9 ; i++ )   
      va1 [ i ] =  10 * i;  
   valarray<double> va2 ( 9 );  
  
   cout << "Initial valarray:";  
   for ( i = 0 ; i < 9 ; i++ )  
      cout << " " << va1 [ i ];  
   cout << endl;  
  
   va2 = log ( va1 );  
   cout << "The natural logarithm of the initial valarray is:\n";  
   for ( i = 0 ; i < 9 ; i++ )  
      cout << va2 [ i ] << endl;  
}  
```  
  
 **Initial valarray: 0 10 20 30 40 50 60 70 80**  
**The natural logarithm of the initial valarray is:**  
**-1.#INF**  
**2.30259**  
**2.99573**  
**3.4012**  
**3.68888**  
**3.91202**  
**4.09434**  
**4.2485**  
**4.38203**   
## Requirements  
 **Header:** <valarray\>  
  
 **Namespace:** std  
  
## See Also  
 [exp, log, and log10](../vs140/exp--log--and-log10.md)