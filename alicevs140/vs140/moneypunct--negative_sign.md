---
title: "moneypunct::negative_sign"
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
ms.assetid: 66180156-bf6d-4a83-ada0-6e5eb6eb0d83
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::negative_sign
Returns a locale-specific sequence of elements to use as a negative sign symbol.  
  
## Syntax  
  
```  
string_type negative_sign( ) const;  
```  
  
## Return Value  
 Returns a locale-specific sequence of elements to use as a negative sign symbol.  
  
## Remarks  
 The member function returns [do_negative_sign](../vs140/moneypunct--do_negative_sign.md).  
  
## Example  
  
```  
// moneypunct_neg_sign.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
#include <sstream>  
  
using namespace std;  
  
int main( )  
{  
   locale loc( "german_germany" );  
  
   const moneypunct <char, true> &mpunct =   
      use_facet <moneypunct <char, true> >(loc);  
   cout << loc.name( ) << " international negative sign: "  
        << mpunct.negative_sign( ) << endl;  
  
   const moneypunct <char, false> &mpunct2 =   
      use_facet <moneypunct <char, false> >(loc);  
   cout << loc.name( ) << " domestic negative sign: "  
        << mpunct2.negative_sign( ) << endl;  
  
   locale loc2( "French" );  
  
   const moneypunct <char, true> &mpunct3 =   
      use_facet <moneypunct <char, true> >(loc2);  
   cout << loc2.name( ) << " international negative sign: "  
        << mpunct3.negative_sign( ) << endl;  
  
   const moneypunct <char, false> &mpunct4 =   
      use_facet <moneypunct <char, false> >(loc2);  
   cout << loc2.name( ) << " domestic negative sign: "  
        << mpunct4.negative_sign( ) << endl;  
};  
```  
  
 **German_Germany.1252 international negative sign: -**  
**German_Germany.1252 domestic negative sign: -**  
**French_France.1252 international negative sign: -**  
**French_France.1252 domestic negative sign: -**   
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)