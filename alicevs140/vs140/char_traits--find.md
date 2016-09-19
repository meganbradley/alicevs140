---
title: "char_traits::find"
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
ms.assetid: bf374b73-d82b-4292-bfdb-618cce4d312d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits::find
Searches for the first occurrence of a specified character in a range of characters.  
  
## Syntax  
  
```  
  
      static const char  
      _  
      type* find(  
   const char_type* _Str,   
   size_t _Num,   
   const char_type& _Ch   
);  
```  
  
#### Parameters  
 `_Str`  
 The first character in the string to be searched.  
  
 `_Num`  
 The number of positions, counting from the first, in the range to be searched.  
  
 `_Ch`  
 The character to be searched for in the range.  
  
## Return Value  
 A pointer to the first occurrence of the specified character in the range if a match is found; otherwise, a null pointer.  
  
## Example  
  
```  
// char_traits_find.cpp  
// compile with: /EHsc  
#include <string>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
  
   const char* s1 = "f2d-1234-abcd";  
   const char* result1;  
   cout << "The string to be searched is: " << s1 << endl;  
  
   // Searching for a 'd' in the first 6 positions of string s1  
   result1 = char_traits<char>::find ( s1 , 6 , 'd');  
   cout << "The character searched for in s1 is: "  
        << *result1 << endl;  
   cout << "The string beginning with the first occurrence\n "  
        << "of the character 'd' is: " << result1 << endl;  
  
   // When no match is found the NULL value is returned  
   const char* result2;  
   result2 = char_traits<char>::find ( s1 , 3 , 'a');  
   if ( result2 == NULL )  
      cout << "The result2 of the search is NULL." << endl;  
   else  
      cout << "The result2 of the search  is: " << result1  
           << endl;  
}  
```  
  
 **The string to be searched is: f2d-1234-abcd**  
**The character searched for in s1 is: d**  
**The string beginning with the first occurrence**  
 **of the character 'd' is: d-1234-abcd**  
**The result2 of the search is NULL.**   
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Struct](../vs140/char_traits-Struct.md)