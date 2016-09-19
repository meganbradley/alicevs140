---
title: "char_traits::length"
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
ms.assetid: d7ac322a-3930-4641-84d1-6bf57916194f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits::length
Returns the length of a string.  
  
## Syntax  
  
```  
  
      static size  
      _  
      t length(  
   const char_type* _Str  
);  
```  
  
#### Parameters  
 `_Str`  
 The C-string whose length is to be measured.  
  
## Return Value  
 The number of elements in the sequence being measured, not including the null terminator.  
  
## Example  
  
```  
// char_traits_length.cpp  
// compile with: /EHsc  
#include <string>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   const char* str1= "Hello";  
   cout << "The C-string str1 is: " << str1 << endl;  
  
   size_t lenStr1;  
   lenStr1 = char_traits<char>::length ( str1 );  
   cout << "The length of C-string str1 is: "   
        << lenStr1 << "." << endl;  
}  
```  
  
 **The C-string str1 is: Hello**  
**The length of C-string str1 is: 5.**   
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Struct](../vs140/char_traits-Struct.md)