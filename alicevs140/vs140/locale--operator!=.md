---
title: "locale::operator!="
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
ms.assetid: 21af069f-7a01-45e9-8af3-492296e62763
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# locale::operator!=
Tests two locales for inequality.  
  
## Syntax  
  
```  
bool operator!=(  
    const locale& _Right  
) const;  
```  
  
#### Parameters  
 `_Right`  
 One of the locales to be tested for inequality.  
  
## Return Value  
 A Boolean value that is **true** if the locales are not copies of the same locale; **false** if the locales are copies of the same locale.  
  
## Remarks  
 Two locales are equal if they are the same locale, if one is a copy of the other, or if they have identical names.  
  
## Example  
  
```  
// locale_op_ne.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <string>  
#include <locale>  
  
using namespace std;  
  
int main( )   
{  
   locale loc1( "German_Germany" );  
   locale loc2( "German_Germany" );  
   locale loc3( "English" );  
  
   if ( loc1 != loc2 )  
      cout << "locales loc1 (" << loc1.name( )  
      << ") and\n loc2 (" << loc2.name( ) << ") are not equal." << endl;  
   else  
      cout << "locales loc1 (" << loc1.name( )  
      << ") and\n loc2 (" << loc2.name( ) << ") are equal." << endl;  
  
   if ( loc1 != loc3 )  
      cout << "locales loc1 (" << loc1.name( )  
      << ") and\n loc3 (" << loc3.name( ) << ") are not equal." << endl;  
   else  
      cout << "locales loc1 (" << loc1.name( )  
      << ") and\n loc3 (" << loc3.name( ) << ") are equal." << endl;  
}  
```  
  
 **locales loc1 (German_Germany.1252) and**  
 **loc2 (German_Germany.1252) are equal.**  
**locales loc1 (German_Germany.1252) and**  
 **loc3 (English_United States.1252) are not equal.**   
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [locale Class](../vs140/locale-Class.md)