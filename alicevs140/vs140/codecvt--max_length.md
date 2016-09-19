---
title: "codecvt::max_length"
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
ms.assetid: 40439217-7934-4ebb-9985-f6d14d9e1678
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# codecvt::max_length
Returns the maximum number of external **Byte**s necessary to produce one internal **CharType**.  
  
## Syntax  
  
```  
int max_length( ) const throw( );  
```  
  
## Return Value  
 The maximum number of **Byte**s necessary to produce one **CharType**.  
  
## Remarks  
 The member function returns [do_max_length](../vs140/codecvt--do_max_length.md).  
  
## Example  
  
```  
// codecvt_max_length.cpp  
// compile with: /EHsc  
#define _INTL  
#include <locale>  
#include <iostream>  
using namespace std;  
  
int main( )     
{  
   locale loc( "C");//English_Britain" );//German_Germany  
   int res = use_facet<codecvt<char, char, mbstate_t> >  
     ( loc ).max_length( );  
   wcout << res << endl;  
}  
```  
  
 **1**   
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [codecvt Class](../vs140/codecvt-Class.md)