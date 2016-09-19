---
title: "islower"
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
ms.assetid: b95bf7f6-dd52-4174-8a29-19c6980bd6a8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# islower
Tests whether an element in a locale is lower case.  
  
## Syntax  
  
```  
  
   template<Class CharType>  
bool islower(  
   CharType _Ch,   
   const locale& _Loc  
)  
```  
  
#### Parameters  
 `_Ch`  
 The element to be tested.  
  
 `_Loc`  
 The locale containing the element to be tested.  
  
## Return Value  
 **true** if the element tested is a lowercase character; **false** if it is not.  
  
## Remarks  
 The template function returns [use_facet](../vs140/use_facet.md)<[ctype](../vs140/ctype-Class.md)<**CharType**> >(`_Loc`). [is](../vs140/ctype--is.md)(**ctype**<**CharType**>::**lower**, `_Ch`).  
  
## Example  
  
```  
// locale_islower.cpp  
// compile with: /EHsc  
#include <locale>  
#include <iostream>  
  
using namespace std;  
  
int main( )     
{  
   locale loc ( "German_Germany" );  
   bool result1 = islower ( 'L', loc );  
   bool result2 = islower ( 'n', loc );  
   bool result3 = islower ( '3', loc );  
  
   if ( result1 )  
      cout << "The character 'L' in the locale is "  
           << "a lowercase character." << endl;  
   else  
      cout << "The character 'L' in the locale is "  
           << " not a lowercase character." << endl;  
  
   if ( result2 )  
      cout << "The character 'n' in the locale is "  
           << "a lowercase character." << endl;  
   else  
      cout << "The character 'n' in the locale is "  
           << " not a lowercase character." << endl;  
  
   if ( result3 )  
      cout << "The character '3' in the locale is "  
           << "a lowercase character." << endl;  
   else  
      cout << "The character '3' in the locale is "  
           << " not a lowercase character." << endl;  
}  
```  
  
## Output  
  
```  
The character 'L' in the locale is  not a lowercase character.  
The character 'n' in the locale is a lowercase character.  
The character '3' in the locale is  not a lowercase character.  
```  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std