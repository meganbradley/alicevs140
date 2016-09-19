---
title: "tanh (&lt;valarray&gt;)"
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
ms.assetid: 745836cc-c237-468b-a219-ace73fce5ec1
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# tanh (&lt;valarray&gt;)
Operates on the elements of an input valarray, returning a valarray whose elements are equal to the hyperbolic tangent of the elements of the input valarray.  
  
## Syntax  
  
```  
  
   template<class Type>  
valarray<Type> tanh(  
   const valarray<Type>& _Left  
);  
```  
  
#### Parameters  
 `_Left`  
 The input valarray whose elements are to be operated on by the member function.  
  
## Return Value  
 A valarray whose elements are equal to the hyperbolic cosine of the elements of the input valarray.  
  
## Remarks  
 Identities defining the hyperbolic tangent in terms of the exponential function:  
  
 tanh ( *z* ) = sinh ( *z* ) / cosh ( *z* ) = ( exp ( *z* ) – exp ( -*z* ) ) / ( exp ( *z* ) + exp ( -*z* ) )  
  
## Example  
  
```  
// valarray_tanh.cpp  
// compile with: /EHsc  
#include <valarray>  
#include <iostream>  
#include <iomanip>  
  
int main( )  
{  
   using namespace std;  
   double pi = 3.14159265359;  
   int i;  
  
   valarray<double> va1 ( 9 );  
   for ( i = 0 ; i < 9 ; i++ )   
      va1 [ i ] =  pi * ( 0.25 * i - 1 );  
   valarray<double> va2 ( 9 );  
  
   cout << "The initial valarray is:\n";  
   for ( i = 0 ; i < 9 ; i++ )  
      cout << setw( 10 ) << va1 [ i ]  
      << "   radians, which is     "  
                    << setw( 5 ) << ( 180/pi ) * va1 [ i ]  
                    << "  degrees" << endl;  
   cout << endl;  
  
   va2 = tanh ( va1 );  
   cout << "The hyperbolic tangent of the initial valarray is:\n";  
   for ( i = 0 ; i < 9 ; i++ )  
     cout << va2 [ i ] << endl;  
}  
```  
  
 **The initial valarray is:**  
 **-3.14159   radians, which is      -180  degrees**  
 **-2.35619   radians, which is      -135  degrees**  
 **-1.5708   radians, which is       -90  degrees**  
 **-0.785398   radians, which is       -45  degrees**  
 **0   radians, which is         0  degrees**  
 **0.785398   radians, which is        45  degrees**  
 **1.5708   radians, which is        90  degrees**  
 **2.35619   radians, which is       135  degrees**  
 **3.14159   radians, which is       180  degrees**  
**The hyperbolic tangent of the initial valarray is:**  
**-0.996272**  
**-0.982193**  
**-0.917152**  
**-0.655794**  
**0**  
**0.655794**  
**0.917152**  
**0.982193**  
**0.996272**   
## Requirements  
 **Header:** <valarray\>  
  
 **Namespace:** std