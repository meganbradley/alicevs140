---
title: "moneypunct::thousands_sep"
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
ms.assetid: e2527cae-012f-4b5a-a636-bed6705c15f4
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# moneypunct::thousands_sep
Returns a locale-specific sequence of elements to use as a thousands separator symbol.  
  
## Syntax  
  
```  
CharType thousands_sep( ) const;  
```  
  
## Return Value  
 A locale-specific sequence of elements to use as a thousands separator  
  
## Remarks  
 The member function returns [do_thousands_sep](../vs140/moneypunct--do_thousands_sep.md).  
  
## Example  
  
```  
// moneypunct_thou_sep.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
#include <sstream>  
using namespace std;  
int main( )  
{  
   locale loc( "german_germany" );  
  
   const moneypunct <char, true> &mpunct =   
       use_facet <moneypunct <char, true > >(loc);  
   cout << loc.name( ) << " international thousands separator: "  
        << mpunct.thousands_sep( ) << endl;  
  
   const moneypunct <char, false> &mpunct2 =   
      use_facet <moneypunct <char, false> >(loc);  
   cout << loc.name( ) << " domestic thousands separator: "  
        << mpunct2.thousands_sep( ) << endl << endl;  
  
   locale loc2( "english_canada" );  
  
   const moneypunct <char, true> &mpunct3 =   
       use_facet <moneypunct <char, true> >(loc2);  
   cout << loc2.name( ) << " international thousands separator: "  
        << mpunct3.thousands_sep( ) << endl;  
  
   const moneypunct <char, false> &mpunct4 =   
      use_facet <moneypunct <char, false> >(loc2);  
   cout << loc2.name( ) << " domestic thousands separator: "  
        << mpunct4.thousands_sep( ) << endl;  
}  
```  
  
 **German_Germany.1252 international thousands separator: .**  
**German_Germany.1252 domestic thousands separator: .**  
**English_Canada.1252 international thousands separator: ,**  
**English_Canada.1252 domestic thousands separator: ,**   
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [moneypunct Class](../vs140/moneypunct-Class.md)