---
title: "numpunct::thousands_sep"
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
ms.assetid: 8ad23de8-15d6-4b76-94d0-a64124a9ec33
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# numpunct::thousands_sep
Returns a locale-specific element to use as a thousands separator.  
  
## Syntax  
  
```  
CharType thousands_sep( ) const;  
```  
  
## Return Value  
 A locale-specific element to use as a thousands separator.  
  
## Remarks  
 The member function returns [do_thousands_sep](../vs140/numpunct--do_thousands_sep.md).  
  
## Example  
  
```  
// numpunct_thou_sep.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
#include <sstream>  
using namespace std;  
int main( )  
{  
   locale loc( "german_germany" );  
  
   const numpunct <char> &npunct =   
   use_facet < numpunct < char > >( loc );  
   cout << loc.name( ) << " decimal point "<<   
   npunct.decimal_point( ) << endl;  
   cout << loc.name( ) << " thousands separator "   
   << npunct.thousands_sep( ) << endl;  
};  
```  
  
 **German_Germany.1252 decimal point ,**  
**German_Germany.1252 thousands separator .**   
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [numpunct Class](../vs140/numpunct-Class.md)